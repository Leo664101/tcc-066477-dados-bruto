# Dados brutos: API unificada × Backend For Frontend

Dados brutos do Trabalho de Conclusão de Curso **Avaliação da Eficiência de Desempenho e Latência em Arquiteturas Backend For Frontend (BFF)**, de Leonardo Pertile Follador (Ciência da Computação, URI Erechim, 2026). O código, os scripts de execução e análise e as evidências compactas da campanha principal estão no [repositório principal](https://https.git.uricer.edu.br/mlucas/tcc-066477-leonardo).

Estes arquivos ficaram fora do repositório principal porque ultrapassam o limite de tamanho do servidor Git da universidade. Eles foram copiados sem alteração, como gerados pelos scripts.

## Conteúdo

- `results/`: pastas originais das execuções.
  - **Campanha principal:** 26 pastas `campanha-20261019T...` e `campanha-20261020T...`. São os 24 pares válidos e as duas tentativas invalidadas por agenda incompleta (`campanha-20261020T003637Z-aeaeab93` e `campanha-20261020T143106Z-435b7571`). A relação entre cada posição da campanha e sua pasta está em `docs/principal-execucoes.json`, no repositório principal.
  - **Registro do congelamento:** `principal-v1-registro/`, com os hashes das fontes, dos JARs e das imagens, as versões do Docker e do JMeter e a cópia do protocolo usada na coleta.
  - **Pilotos e validações:** as 38 pastas descritas em [evidencias-pilotos](evidencias-pilotos/README.md). As execuções que não entram em nenhuma análise, como as do protótipo com banco de dados, não foram incluídas.
- `evidencias-pilotos/`: seleção compacta dos pilotos, com inventário de hashes e a descrição de cada pasta.

Nas pastas da campanha principal, cada execução tem a configuração, a janela de medição, o JTL bruto e o da medição, as agendas de chegada, a auditoria do gerador, as séries de CPU e memória, os registros da rede emulada e os logs. Os relatórios antigos podem conter caminhos absolutos do computador da coleta.

## Recalcular a análise da campanha principal

1. Clone o repositório principal e copie o conteúdo de `results/` deste repositório para `benchmarks/results/`.
2. Na raiz do repositório principal, com Python 3.11 ou superior:

```powershell
python -m pip install -r scripts/requirements-analise.txt
python scripts/consolidar-principal.py --registro docs/principal-execucoes.json --saida benchmarks/results/principal-recalculada --graficos
```

O resultado pode ser comparado com `benchmarks/evidencias-principal`, no repositório principal. O arquivo `fontes.json` dessa pasta registra o SHA-256 de cada arquivo bruto usado na análise.

## Integridade

O `.gitattributes` deste repositório desativa a conversão de quebras de linha (`* -text`), para que os arquivos mantenham os bytes originais e os hashes possam ser conferidos diretamente.
