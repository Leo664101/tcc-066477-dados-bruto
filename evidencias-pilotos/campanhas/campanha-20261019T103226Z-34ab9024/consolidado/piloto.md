# Relatorio exploratorio do piloto

Criterios piloto v1: triagem heuristica, sem aprovar parametros oficiais. Ver piloto.json para valores, contagens e limites. Falhas tecnicas permanecem excluidas; falhas HTTP nao sao apagadas.

| Execucao | Perfil | Estado tecnico | Erros HTTP brutos da execucao | Aquecimento | Duracao |
| --- | --- | --- | --- | --- | --- |
| netem0-pedidos-taxa160-m50-50-r1-unificada | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa160-m50-50-r1-unificada | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa160-m50-50-r1-bff | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa160-m50-50-r1-bff | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |

## Variabilidade entre execucoes

- bff/mobile, condicao 69d988c65efb2a460c47ed80623b55a1b1df723d2338bdcc5b44a08fff16e4a8: N=1, CV=indisponivel; dados-insuficientes.
- bff/web, condicao 69d988c65efb2a460c47ed80623b55a1b1df723d2338bdcc5b44a08fff16e4a8: N=1, CV=indisponivel; dados-insuficientes.
- unificada/mobile, condicao 8cfed2f28527db51b1c819ec262218811d08ff329d9d817bb8bb4bde3e562ef0: N=1, CV=indisponivel; dados-insuficientes.
- unificada/web, condicao 8cfed2f28527db51b1c819ec262218811d08ff329d9d817bb8bb4bde3e562ef0: N=1, CV=indisponivel; dados-insuficientes.
