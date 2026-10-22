# Relatorio exploratorio do piloto

Criterios piloto v1: triagem heuristica, sem aprovar parametros oficiais. Ver piloto.json para valores, contagens e limites. Falhas tecnicas permanecem excluidas; falhas HTTP nao sao apagadas.

| Execucao | Perfil | Estado tecnico | Erros HTTP brutos da execucao | Aquecimento | Duracao |
| --- | --- | --- | --- | --- | --- |
| netem25-pedidos-taxa40-m50-50-r1-bff | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem25-pedidos-taxa40-m50-50-r1-bff | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem25-pedidos-taxa40-m50-50-r1-unificada | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem25-pedidos-taxa40-m50-50-r1-unificada | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |

## Variabilidade entre execucoes

- bff/mobile, condicao ac17bf24013d85b0afa5eee05c13c9773be8061c7682e993ef9b7ce7613844ea: N=1, CV=indisponivel; dados-insuficientes.
- bff/web, condicao ac17bf24013d85b0afa5eee05c13c9773be8061c7682e993ef9b7ce7613844ea: N=1, CV=indisponivel; dados-insuficientes.
- unificada/mobile, condicao bd8a6260343baf4be4f5c50534260fbff87faa8fc24379f5b12e88469c99d543: N=1, CV=indisponivel; dados-insuficientes.
- unificada/web, condicao bd8a6260343baf4be4f5c50534260fbff87faa8fc24379f5b12e88469c99d543: N=1, CV=indisponivel; dados-insuficientes.
