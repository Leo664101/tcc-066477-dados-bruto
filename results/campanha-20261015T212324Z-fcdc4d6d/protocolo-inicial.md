# Proposta inicial do piloto

Versão de planejamento de 15/10/2026. Nenhuma rodada do piloto foi executada por este documento. As escolhas abaixo são propostas operacionais para avaliar, não parâmetros oficiais ou valores garantidos pela literatura. A matriz da campanha principal será definida depois dos resultados do piloto.

## Base disponível e objetivo

Produtos e pedidos estão implementados e têm equivalência funcional verificada nas duas arquiteturas. Há verificações técnicas curtas a 20 operações/s, emulação 0/25 ms por sentido, auditoria de agenda/rede e monitor opcional do JMeter. A tentativa com atraso de 272 ms permanece inválida; as verificações posteriores aprovadas não a substituem. Ver [carga por taxa](carga-por-taxa.md), [rede](rede-experimental.md) e [gerador](diagnostico-gerador.md).

O primeiro objetivo é testar se o procedimento sustenta a carga e produz comportamento suficientemente estável para escolher aquecimento, medição e repetições. Não é demonstrar superioridade de uma arquitetura nem encontrar saturação já na primeira bateria.

## Condições comuns propostas

| Item | Valor inicial | Motivo e interpretação |
| --- | --- | --- |
| Arquiteturas | API unificada e alternativa BFF com Web + Mobile juntos | Mesma necessidade funcional por perfil; uma alternativa por vez |
| Clientes | 50% Web / 50% Mobile por operações agendadas | Reduz combinações; 80/20 e 20/80 ficam fora deste piloto inicial |
| Dados internos | JSONs atuais; atraso interno de 0 ms nos três serviços; sem banco/cache de respostas | Evita acrescentar outro fator nesta primeira bateria |
| Taxas totais | 20 op/s; exploração posterior de 40 op/s | 20 tem evidência técnica curta; 40 é dobra candidata, não carga alta comprovada. Cada perfil recebe 10 ou 20 op/s |
| Rede | Roteador com 0 ms; exploração de 25 ms por sentido | Mesma topologia, só cliente–entrada; sem banda limitada, perda ou jitter. 0 ms artificial não significa latência real zero |
| Executores do gerador | 8 por perfil | Mantém configuração técnica anterior; não garante capacidade em condições maiores |
| Atraso máximo de chegada | 250 ms em todas as fases | Mantém auditoria anterior, inclusive na subida; não aumentar apenas para aprovar rodadas |
| Tempos HTTP | Conexão 2 s, resposta 15 s, limite total 17 s, drenagem máxima 20 s | Valores atualmente implementados; falhas/timeouts são preservados |
| Preparação após saúde/checagens | 30 s sem carga experimental | Janela operacional fixa; não é warm-up nem prova de estabilização da JVM |
| Subida | 30 s | Rampa da taxa até o alvo |
| Aquecimento | 120 s na taxa alvo | Candidato a avaliar pelos critérios abaixo |
| Medição | 300 s | Mesma duração nas duas arquiteturas, sem selecionar retrospectivamente trechos favoráveis |
| Descanso | 60 s após encerramento dos processos da rodada | Separado da preparação e da inicialização; custo adicional estimado abaixo |
| Reinício | Aplicações/JVMs, roteador e processo JMeter novos por tentativa | Repetições independentes de processo; dados/imagens/configuração preservados |
| Recursos | Limites atuais do Compose, iguais entre repetições | Orçamento agregado da entrada equivalente; BFFs com quotas individuais |
| Instrumentação | Docker stats alvo 2 s, snapshots cgroup e `-DiagnosticarGerador` em todas as rodadas | Mantém observabilidade; CPU de containers ainda diagnóstica, sem alegar método oficial validado |

Usar JMeter no host e Docker no mesmo computador. Reservar a máquina: sem builds, outras campanhas, geração de relatórios pesados ou trabalho interativo deliberado durante as rodadas. Registrar processos concorrentes conhecidos, hardware/versões e incidentes; não desligar serviços de segurança do sistema. Se uma interferência for observada, registrar sua janela/motivo e interromper a sequência para investigar, sem apagar a tentativa. A ausência de atividade conhecida não comprova isolamento.

## Baterias e ordem

Uma condição é a combinação de operação, taxa, rede e demais parâmetros; cada par contém uma execução de cada arquitetura. Uma execução BFF inclui os dois BFFs ativos, não duas execuções independentes.

| Etapa | Operação | Taxa total | Atraso por sentido | Pares | Execuções | Objetivo |
| --- | --- | --- | --- | --- | --- | --- |
| A — primeira bateria | Pedidos (C3, detalhado Web/resumo Mobile) | 20 op/s | 0 ms | 3 | 6 | Avaliar procedimento, aquecimento e variação inicial |
| B1 — exploração | Produtos (C1) | 20 op/s | 0 ms | 1 | 2 | Conferir comportamento do caminho simples |
| B2 — exploração | Pedidos (C3) | 20 op/s | 25 ms | 1 | 2 | Verificar a condição com atraso |
| B3 — exploração | Pedidos (C3) | 40 op/s | 25 ms | 1 | 2 | Verificar capacidade com taxa maior |
| Total inicialmente proposto | | | | 6 | 12 | Não é uma matriz fatorial completa |

Executar primeiro A e revisar seus registros antes de B. Em A, usar pares U–B, B–U, U–B (U = unificada; B = alternativa BFF). Em B1 usar B–U, B2 U–B e B3 B–U, nessa ordem. A ordem é planejada, não aleatorizada; registrar a limitação de variação temporal. Não usar B1/B2/B3, com um par cada, para estimar variabilidade entre repetições ou concluir desempenho comparativo.

Se B revelar uma condição relevante que exija avaliação de variação, propor mais dois pares nessa condição para completar três, em uma nova chamada identificada. Cada ampliação acrescenta quatro execuções. Se o protocolo mudar, as versões não são repetições equivalentes. Não executar automaticamente todas as extensões nem assumir que três pares bastarão para a campanha principal.

## Critérios iniciais de verificação

Os limiares desta seção são heurísticas propostas para o piloto, fixadas antes de sua execução. O PDF prevê aquecimento, controle e repetição (seções 4.4–4.9), mas não fornece estes números. Não são testes estatísticos de estacionariedade nem garantia de precisão.

### Validade técnica

1. Exigir agenda atendida em todas as fases: nenhuma chegada ausente, fora dos limites ou acima da tolerância; conservar a regra existente sobre início antecipado. Falha no gerador invalida a tentativa para comparação sob a taxa solicitada, mesmo se o HTTP funcionar.
2. Exigir auditorias de rede, ambiente e coleta aprovadas: configurações/IDs estáveis, contadores coerentes, ausência de descartes inesperados, arquivos completos e diagnóstico do gerador concluído.
3. Erros HTTP/timeouts com geração válida são resultado observado, não motivo para apagar a rodada. Manter contagens e latências de falhas separadas. Neste piloto de consultas determinísticas, qualquer erro impede avançar automaticamente para B3 até investigar contrato, aplicação, rede e eventual saturação.
4. Se houver falha técnica, parar a progressão. Uma nova tentativa deve ser identificada, justificada e preservada junto à anterior; não repetir até obter sucesso e esconder as falhas.

### Adequação do aquecimento

Dividir o aquecimento em blocos de 30 s. Avaliar os três últimos blocos completos (últimos 90 s), separadamente para Web/Mobile e cada arquitetura, usando operações bem-sucedidas pelo instante de início. Para cada bloco, registrar quantidade, média e mediana da latência; registrar falhas à parte.

Exigir ao menos 200 sucessos por bloco/perfil para esta triagem. Para a média e, separadamente, a mediana dos três blocos, calcular `amplitude = máximo - mínimo` e comparar com `max(1 ms, 10% da mediana dos três valores)`. As duas amplitudes devem ficar dentro desse limite. Conferir também os três primeiros blocos da medição: a mediana de suas médias/medianas deve diferir da correspondente mediana do aquecimento em no máximo o mesmo limite calculado sobre o aquecimento.

Se faltar quantidade suficiente ou ocorrer mudança maior, classificar como “aquecimento não confirmado”, preservando a medição inteira. Não mover o início da janela posteriormente. Inspecionar carga gerada, CPU/memória, GC, erros e interferências; se a hipótese continuar sendo aquecimento insuficiente, propor nova versão com 300 s de warm-up para ambas as arquiteturas na condição afetada. Não estender indefinidamente: após essa primeira ampliação, reavaliar causa/protocolo em vez de ampliar automaticamente.

Examinar séries de CPU/memória como diagnóstico, não usar uma leitura isolada de Docker stats como critério automático de estabilidade. O critério acima verifica latência sob a carga escolhida, não comprova que todos os componentes/JVMs atingiram estado estacionário.

### Duração e variabilidade

- Comparar as duas metades completas da medição (150 s cada), por perfil: diferenças de média e mediana de sucessos acima de `max(1 ms, 10% do valor da primeira metade)` exigem investigação de tendência/interferência. Não escolher a metade melhor.
- Registrar N de sucessos e P95/P99 por execução. A 20 op/s e 50/50, são esperados aproximadamente 3.000 inícios por perfil em 300 s; isso não garante precisão do P99. Se as metades forem discordantes ou a cauda for sensível/pouco amostrada, propor 600 s de medição nas duas arquiteturas e registrar a nova condição.
- Em A, apresentar os três valores por arquitetura/perfil, média, desvio-padrão e coeficiente de variação da latência média (`desvio-padrão amostral / média`). CV acima de 10% é sinal exploratório para investigar, não exclusão automática nem regra de suficiência estatística. CV baixo em três repetições também não comprova precisão.
- Quantidade final de repetições e intervalos de confiança continuam por definir com a variação observada. A margem de 10% anteriormente sugerida para um IC de 95% da média é uma proposta distinta destes limiares de triagem; não foi calculada/aprovada aqui e não se transfere ao P95/P99.

## Tempo previsto

Cada execução tem 450 s de carga (30 + 120 + 300), mais 30 s de preparação e 60 s de descanso: **9 minutos por execução**, sem inicialização, auditorias, drenagem e processamento dos arquivos.

| Escopo | Carga | Preparação + descanso | Subtotal conhecido |
| --- | --- | --- | --- |
| A, seis execuções | 45 min | 9 min | 54 min |
| B1–B3, seis execuções | 45 min | 9 min | 54 min |
| A + B, doze execuções | 90 min | 18 min | 108 min |
| Mais dois pares em uma condição | 30 min | 6 min | 36 min |

Somar tempo real de build/inicialização, auditoria, análise e até 20 s de drenagem por execução (até 4 min para doze). Para reservar agenda, considerar aproximadamente **1 h a 1 h 30 para A** e **2 h a 3 h para A+B**, sem investigação, ampliações ou revisão entre etapas. São margens de planejamento, não tempos medidos de um piloto. Se os números precisarem mudar, recalcular o orçamento antes de iniciar mais rodadas.

## Automação e preparação para a execução

Carga, tempos 30/120/300, pares/alternância dentro de uma campanha, recreação das aplicações, rede, coorte/drenagem, registros e consolidação estão implementados. A atualização de 15/10/2026 acrescenta `-PreparacaoSegundos`, `-DescansoSegundos` e `-AvaliarPiloto` às campanhas. Os dois tempos têm padrão zero para preservar o uso anterior; devem ser informados explicitamente para esta proposta.

`preparacao.json` registra a espera após as checagens iniciais e antes de iniciar a coleta/JMeter. Ela usa relógio monotônico; não é aquecimento. Quando o descanso solicitado é positivo, a campanha para os componentes do projeto após cada tentativa, confirma ausência de containers ativos e só então espera o descanso, registrado em `descanso.json`. Há descanso também após a última tentativa e após falhas. Se nem a pasta da execução existir, o registro de descanso fica na raiz da campanha com o nome da tentativa. Falha no encerramento interrompe a sequência mesmo com `-ContinuarAposFalha`. Não há exclusão de volumes ou resultados.

O relatório `consolidado/piloto.md` e seu detalhamento `piloto.json` avaliam os blocos, metades e CV por arquitetura/perfil/assinatura. Contêm contagens, erros e critérios, sem alterar janelas ou exclusões por estabilidade. Menos de 200 sucessos nos blocos, medição menor que os 300 s da proposta ou menos de três valores para CV gera “dados insuficientes” no respectivo critério; uma rodada curta não será declarada aquecida nem suficiente para avaliar a duração proposta. Erros HTTP são mantidos; estado técnico “incluída” não significa ausência de erros. Nenhum relatório inicia a etapa B, aumenta tempos ou aprova a campanha principal automaticamente.

**Os comandos abaixo são apenas planejamento.** Retirar `-SomentePlanejar` iniciará carga real e exige `-JMeterHome` ou `JMETER_HOME` configurado. A verificação técnica curta do ciclo completo com os novos parâmetros passou, conforme evidências abaixo. Antes da bateria longa, confirmar ambiente reservado e revisar os incidentes/condições que não são automaticamente observáveis. Não interpretar a automação como confirmação de ausência de interferência ou decisão metodológica final.

```powershell
$comum = @{
    Rede = 'netem'; Misturas = @('50/50'); MaximoEmVooPorPerfil = 8
    AtrasoMaximoMs = 250; SubidaSegundos = 30; AquecimentoSegundos = 120
    DuracaoSegundos = 300; DiagnosticarGerador = $true; SomentePlanejar = $true
    PreparacaoSegundos = 30; DescansoSegundos = 60; AvaliarPiloto = $true
}
& ./scripts/executar-campanha.ps1 @comum -Operacao pedidos -TaxasPorSegundo @(20) -AtrasosRedeMs @(0) -Repeticoes 3
& ./scripts/executar-campanha.ps1 @comum -Operacao produtos -TaxasPorSegundo @(20) -AtrasosRedeMs @(0) -Repeticoes 1 -PrimeiroCenario bff
& ./scripts/executar-campanha.ps1 @comum -Operacao pedidos -TaxasPorSegundo @(20) -AtrasosRedeMs @(25) -Repeticoes 1
& ./scripts/executar-campanha.ps1 @comum -Operacao pedidos -TaxasPorSegundo @(40) -AtrasosRedeMs @(25) -Repeticoes 1 -PrimeiroCenario bff
```

Ao executar futuramente, registrar em cada pasta a versão desta proposta, etapa, par, ordem real, horários das esperas, incidentes e decisão após a análise. Preservar dados de A/B separados de verificações técnicas anteriores e da campanha principal. O usuário continua responsável pelos commits; este planejamento não publica nem executa nada.

Para refazer a avaliação sem gerar carga: `& ./scripts/analisar-piloto.ps1 -Pasta benchmarks/results/campanha-<id>`. O comando reconsolida e audita os registros, depois gera os relatórios; preserva arquivos brutos, mas atualiza os derivados. Não é o futuro HTML consolidado, que permanece pendente.

### Validação da automação em 15/10/2026

Passaram testes de mediana, piso de 1 ms, fronteiras dos blocos/janela, separação de falhas e sucessos, amostra insuficiente, mudança após warm-up, CV alto/baixo e reanálise. A auditoria rejeita espera ausente ou menor que a declarada e separa parâmetros de espera na assinatura. Teste de ciclo com Docker/JMeter substituídos em uma cópia isolada conferiu ordem iniciar–carga–parar–descanso, parada após falha e preservação das próximas tentativas como pendentes. Esperas reais de um segundo foram verificadas. Após os testes controlados, duas rodadas curtas Docker/JMeter validaram a integração, conforme registro abaixo. O piloto longo não foi executado.

Comandos reproduzíveis sem Docker: `scripts/testes/testar-criterios-piloto.ps1`, `scripts/testes/testar-ciclo-campanha.ps1` e `scripts/testes/testar-consolidacao.ps1`. O relatório usa critérios `criterios-piloto-v1`; a versão e hashes dos scripts ficam no JSON. A coleta automática não decide a suficiência do P99, do número final de repetições ou do método definitivo de CPU.

A campanha técnica `campanha-20261015T160545Z-2846b2ab` usou produtos, 20 op/s, 50/50, netem 0 ms, oito executores por perfil, tolerância de 250 ms, tempos 2/5/15 s e esperas de um segundo, com monitor do gerador e avaliação habilitados. Ambas as arquiteturas cumpriram a agenda, tiveram zero erros HTTP e entraram no consolidado (2/2). Preparação e descanso foram registrados em ambas; os containers foram encerrados. O relatório final indica dados insuficientes para aquecimento, duração de 300 s e CV com uma repetição por arquitetura. Esse resultado confirma a distinção entre teste técnico e piloto; não comprova estabilidade.

Evidências: `benchmarks/results/campanha-20261015T160545Z-2846b2ab/consolidado/piloto.md` e `piloto.json`; log `tmp/ciclo-piloto-integracao-20261015.log`. A avaliação foi reprocessada após explicitar a exigência mínima de 300 s para o critério de duração, preservando os brutos. Verificação de sintaxe e testes de consolidação/critério passaram. Código Java não alterado; não houve novos testes Maven ou commits automáticos.
