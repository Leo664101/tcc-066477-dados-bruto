# Relatorio exploratorio do piloto

Criterios piloto v1: triagem heuristica, sem aprovar parametros oficiais. Ver piloto.json para valores, contagens e limites. Falhas tecnicas permanecem excluidas; falhas HTTP nao sao apagadas.

| Execucao | Perfil | Estado tecnico | Erros HTTP brutos da execucao | Aquecimento | Duracao |
| --- | --- | --- | --- | --- | --- |
| netem0-pedidos-taxa80-m50-50-r1-unificada | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa80-m50-50-r1-unificada | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa80-m50-50-r1-bff | web | excluida |  | nao-avaliado | nao-avaliado |
| netem0-pedidos-taxa80-m50-50-r1-bff | mobile | excluida |  | nao-avaliado | nao-avaliado |

## Variabilidade entre execucoes

- unificada/mobile, condicao 4141e362db2a7a073f4c8c2f98115e0c3023e4e87faee20b1fb222fd9448a4c5: N=1, CV=indisponivel; dados-insuficientes.
- unificada/web, condicao 4141e362db2a7a073f4c8c2f98115e0c3023e4e87faee20b1fb222fd9448a4c5: N=1, CV=indisponivel; dados-insuficientes.
