# Relatorio exploratorio do piloto

Criterios piloto v1: triagem heuristica, sem aprovar parametros oficiais. Ver piloto.json para valores, contagens e limites. Falhas tecnicas permanecem excluidas; falhas HTTP nao sao apagadas.

| Execucao | Perfil | Estado tecnico | Erros HTTP brutos da execucao | Aquecimento | Duracao |
| --- | --- | --- | --- | --- | --- |
| netem25-pedidos-taxa160-m50-50-r1-bff | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem25-pedidos-taxa160-m50-50-r1-bff | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem25-pedidos-taxa160-m50-50-r1-unificada | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem25-pedidos-taxa160-m50-50-r1-unificada | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |

## Variabilidade entre execucoes

- bff/mobile, condicao 4687b584de43768c5ec64eb7901e5ab2854991d8d59709fdac7c05c3d68e6eb0: N=1, CV=indisponivel; dados-insuficientes.
- bff/web, condicao 4687b584de43768c5ec64eb7901e5ab2854991d8d59709fdac7c05c3d68e6eb0: N=1, CV=indisponivel; dados-insuficientes.
- unificada/mobile, condicao e525ec82a599cde8f5e1e3e5c83cb5b3c9b5d419a1e864d55832a7ead1e242c8: N=1, CV=indisponivel; dados-insuficientes.
- unificada/web, condicao e525ec82a599cde8f5e1e3e5c83cb5b3c9b5d419a1e864d55832a7ead1e242c8: N=1, CV=indisponivel; dados-insuficientes.
