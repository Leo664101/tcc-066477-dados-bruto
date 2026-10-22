# Relatorio exploratorio do piloto

Criterios piloto v1: triagem heuristica, sem aprovar parametros oficiais. Ver piloto.json para valores, contagens e limites. Falhas tecnicas permanecem excluidas; falhas HTTP nao sao apagadas.

| Execucao | Perfil | Estado tecnico | Erros HTTP brutos da execucao | Aquecimento | Duracao |
| --- | --- | --- | --- | --- | --- |
| netem0-pedidos-taxa40-m50-50-r1-bff | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa40-m50-50-r1-bff | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa40-m50-50-r1-unificada | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa40-m50-50-r1-unificada | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |

## Variabilidade entre execucoes

- bff/mobile, condicao b4b53637a03730bc37dc35be1074139207b23efa2aaa1d93f525dcc31f6afd2d: N=1, CV=indisponivel; dados-insuficientes.
- bff/web, condicao b4b53637a03730bc37dc35be1074139207b23efa2aaa1d93f525dcc31f6afd2d: N=1, CV=indisponivel; dados-insuficientes.
- unificada/mobile, condicao d40165b5da7cb9c8a4cbbc02044c56eeea35ea9210d333fa4b560bea9b1b32d8: N=1, CV=indisponivel; dados-insuficientes.
- unificada/web, condicao d40165b5da7cb9c8a4cbbc02044c56eeea35ea9210d333fa4b560bea9b1b32d8: N=1, CV=indisponivel; dados-insuficientes.
