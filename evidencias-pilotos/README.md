# Evidências dos pilotos e validações

Arquivos das execuções feitas antes da campanha principal: validação do ambiente, primeiros testes da carga por taxa e da rede emulada, piloto, exploração de carga e validação da medição de CPU. **Nenhuma destas execuções faz parte dos resultados do TCC.** Cada pasta tem condição e versão próprias, e elas não formam repetições de um mesmo experimento.

O pacote tem 619 arquivos, cerca de 2,55 MiB, e cobre as 38 pastas usadas nessa fase. Os arquivos foram copiados sem alteração, por isso alguns relatórios antigos trazem caminhos absolutos do computador da coleta e classificações da época em que foram gerados.

## Conteúdo

- `campanhas/`: consolidados, manifestos, configurações, janelas de medição, resumos da geração de carga, auditorias de rede e resumos das análises.
- `validacao-rede/`: resultado, amostras HTTP e auditorias da validação inicial do roteador, nas duas arquiteturas, com 0 e 25 ms por sentido.
- `inventario.json`: caminho original, tamanho e SHA-256 de cada arquivo de origem. O campo `arquivoNoPacote` indica a cópia incluída aqui; quando ele é `null`, o arquivo está só nos dados brutos, em `results/`.

Os JTLs, as agendas completas, as séries de recursos e os logs estão nas pastas correspondentes de `results/`. Nos caminhos de `origem` do inventário, `benchmarks/results/<pasta>` corresponde a `results/<pasta>` neste repositório. Os arquivos que vieram de `tmp/rede-integracao-1xmr7_2l/` estão todos copiados em `validacao-rede/`. O único arquivo do inventário que não está neste repositório é `registro-piloto.json`, da campanha do piloto A, um registro do início dessa etapa (hash do protocolo, commit e observações sobre o ambiente), sem medições.

## Pastas

| Pasta | O que contém |
| --- | --- |
| `20261013T112532Z-unificada-4d1c393a` | Verificação do ambiente Docker sem banco, cenário API unificada (modelo fechado, 2 usuários) |
| `20261013T112630Z-bff-31a50dd1` | A mesma verificação no cenário BFF |
| `campanha-20261013T222045Z-a800873a` | Primeiro teste da carga por taxa, anterior à correção do timeout total; não vale como evidência da configuração final |
| `campanha-20261013T222443Z-937e591f` | Segundo teste da carga por taxa, também anterior a essa correção |
| `campanha-20261013T222949Z-7b73a079` | Validação da carga por taxa com produtos, 20 op/s, mistura 50/50 |
| `campanha-20261013T223203Z-88dbb651` | Validação da carga por taxa com pedidos, 20 op/s, mistura 80/20 |
| `campanha-20261014T184341Z-034fa33a` | Tentativa inválida com carga por taxa e roteador: as primeiras chegadas de cada perfil atrasaram 272 ms na rampa |
| `campanha-20261014T184631Z-462c742e` | Integração da rede emulada às campanhas: produtos, modelo fechado, duas arquiteturas com 0 e 25 ms |
| `campanha-20261015T105139Z-05727947` | Repetição diagnóstica da tentativa inválida acima, com agenda cumprida nas duas arquiteturas |
| `campanha-20261015T105955Z-0a3be2e6` | Validação do monitoramento do processo do JMeter (CPU, memória, GC) |
| `campanha-20261015T160545Z-2846b2ab` | Teste técnico da automação do piloto (esperas, triagem e relatórios) |
| `campanha-20261015T212324Z-fcdc4d6d` | Piloto A: pedidos, 20 op/s, 0 ms, três pares, aquecimento de 120 s |
| `campanha-20261016T103818Z-5f0bee35` | Piloto B1: produtos, 20 op/s, 0 ms |
| `campanha-20261016T110018Z-d6e7c8fe` | Piloto B2: pedidos, 20 op/s, 25 ms por sentido |
| `campanha-20261016T112316Z-651cd24d` | Piloto B3: pedidos, 40 op/s, 25 ms por sentido |
| `campanha-20261016T120235Z-10709986` | Par com aquecimento de 300 s (pedidos, 20 op/s, 0 ms), que levou à adoção desse aquecimento |
| `campanha-20261016T155851Z-9ab32a25` | Exploração de carga: pedidos a 40 op/s, 0 ms |
| `campanha-20261016T162708Z-3c35cd3f` | Exploração a 80 op/s, excluída porque a última chegada começou exatamente no fim da janela; levou ao recorte `inicio-coorte-v2` |
| `campanha-20261016T212809Z-f16fcb89` | Exploração a 80 op/s com o recorte corrigido |
| `campanha-20261016T215731Z-168f2e98` | Exploração a 160 op/s, 0 ms |
| `campanha-20261016T222526Z-3b01a784` | Exploração a 160 op/s com 25 ms por sentido; referência para a validação da CPU |
| `campanha-20261017T144922Z-fee237d8` | Tentativa da validação de CPU que falhou antes da carga (`JAVA_HOME` apontando para um caminho inexistente) |
| `campanha-20261017T145319Z-15e95623` | Validação do coletor de CPU na condição P4 |
| `campanha-20261017T152540Z-f2f94c99` | Validação da condição P1 com a instrumentação final |
| `campanha-20261019T100216Z-a9dd4997` | Tentativa da validação de P2 que falhou antes da carga (`JAVA_HOME` inexistente) |
| `campanha-20261019T100507Z-79a2020e` | Validação da condição P2 |
| `campanha-20261019T103226Z-34ab9024` | Validação da condição P3 |
| `capacidade40-20261016` | Recálculo independente da exploração a 40 op/s |
| `capacidade80-v2-20261016` | Recálculo da exploração a 80 op/s com o recorte corrigido |
| `capacidade160-v2-20261016` | Recálculo da exploração a 160 op/s, 0 ms |
| `capacidade160-rede25-20261016` | Recálculo da exploração a 160 op/s com 25 ms |
| `piloto-consolidado-20261016` | Primeira consolidação conjunta dos pilotos A e B |
| `piloto-consolidado-20261016-v2` | Consolidação revisada dos pilotos A e B, que inclui os recursos |
| `piloto-warmup300-20261016` | Recálculo do par com aquecimento de 300 s |
| `cpu1-validacao-20261017` | Recálculo da validação do coletor de CPU (P4) |
| `p1-validacao-20261017` | Recálculo da validação de P1 |
| `p2-validacao-20261019` | Recálculo da validação de P2 |
| `p3-validacao-20261019` | Recálculo da validação de P3 |

## Conferência dos hashes

Para conferir as cópias, calcule o SHA-256 de cada arquivo indicado em `arquivoNoPacote`, com caminho relativo a esta pasta, e compare com os campos `sha256` e `bytes` do inventário. O `.gitattributes` do repositório impede a conversão de quebras de linha, para que os hashes possam ser conferidos diretamente.
