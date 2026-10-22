# Relatorio exploratorio do piloto

Criterios piloto v1: triagem heuristica, sem aprovar parametros oficiais. Ver piloto.json para valores, contagens e limites. Falhas tecnicas permanecem excluidas; falhas HTTP nao sao apagadas.

| Execucao | Perfil | Estado tecnico | Erros HTTP brutos da execucao | Aquecimento | Duracao |
| --- | --- | --- | --- | --- | --- |
| netem0-pedidos-taxa20-m50-50-r1-unificada | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa20-m50-50-r1-unificada | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa20-m50-50-r1-bff | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa20-m50-50-r1-bff | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |

## Variabilidade entre execucoes

- bff/mobile, condicao d083fadda57ebb4fc38a187ba2399b1a1284af6f0b2ae2612410ac3637de498c: N=1, CV=indisponivel; dados-insuficientes.
- bff/web, condicao d083fadda57ebb4fc38a187ba2399b1a1284af6f0b2ae2612410ac3637de498c: N=1, CV=indisponivel; dados-insuficientes.
- unificada/mobile, condicao e08b11dbc85e2c3571110654f6032eb5b9e3b4f166e0313cf917648a0782a1bf: N=1, CV=indisponivel; dados-insuficientes.
- unificada/web, condicao e08b11dbc85e2c3571110654f6032eb5b9e3b4f166e0313cf917648a0782a1bf: N=1, CV=indisponivel; dados-insuficientes.
