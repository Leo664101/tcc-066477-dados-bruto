# Relatorio exploratorio do piloto

Criterios piloto v1: triagem heuristica, sem aprovar parametros oficiais. Ver piloto.json para valores, contagens e limites. Falhas tecnicas permanecem excluidas; falhas HTTP nao sao apagadas.

| Execucao | Perfil | Estado tecnico | Erros HTTP brutos da execucao | Aquecimento | Duracao |
| --- | --- | --- | --- | --- | --- |
| netem0-pedidos-taxa80-m50-50-r1-unificada | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa80-m50-50-r1-unificada | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa80-m50-50-r1-bff | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa80-m50-50-r1-bff | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |

## Variabilidade entre execucoes

- bff/mobile, condicao fcd8518faedc71cb5894ce748323159642d921c36c28bb9138a80465055940c3: N=1, CV=indisponivel; dados-insuficientes.
- bff/web, condicao fcd8518faedc71cb5894ce748323159642d921c36c28bb9138a80465055940c3: N=1, CV=indisponivel; dados-insuficientes.
- unificada/mobile, condicao a12263a2d38893e1ab6892ea5975003b940761697310259fa667d9b53c8d6c6e: N=1, CV=indisponivel; dados-insuficientes.
- unificada/web, condicao a12263a2d38893e1ab6892ea5975003b940761697310259fa667d9b53c8d6c6e: N=1, CV=indisponivel; dados-insuficientes.
