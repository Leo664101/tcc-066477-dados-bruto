# Relatorio exploratorio do piloto

Criterios piloto v1: triagem heuristica, sem aprovar parametros oficiais. Ver piloto.json para valores, contagens e limites. Falhas tecnicas permanecem excluidas; falhas HTTP nao sao apagadas.

| Execucao | Perfil | Estado tecnico | Erros HTTP brutos da execucao | Aquecimento | Duracao |
| --- | --- | --- | --- | --- | --- |
| netem0-pedidos-taxa20-m50-50-r1-unificada | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa20-m50-50-r1-unificada | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa20-m50-50-r1-bff | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa20-m50-50-r1-bff | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa20-m50-50-r2-bff | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa20-m50-50-r2-bff | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa20-m50-50-r2-unificada | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa20-m50-50-r2-unificada | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa20-m50-50-r3-unificada | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa20-m50-50-r3-unificada | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa20-m50-50-r3-bff | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa20-m50-50-r3-bff | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |

## Variabilidade entre execucoes

- bff/mobile, condicao 6ae0cfdae9acde0d7eed7a611bbe624a5444e6c29aa0fd5a78fb32a9977fb7bb: N=3, CV=0.057%; sem-alerta-pela-triagem.
- bff/web, condicao 6ae0cfdae9acde0d7eed7a611bbe624a5444e6c29aa0fd5a78fb32a9977fb7bb: N=3, CV=0.062%; sem-alerta-pela-triagem.
- unificada/mobile, condicao dc96e2e9c9b7ca578a0e3d07e7a7e6a4083867fcd3a2594bc551f04928d58a93: N=3, CV=0.517%; sem-alerta-pela-triagem.
- unificada/web, condicao dc96e2e9c9b7ca578a0e3d07e7a7e6a4083867fcd3a2594bc551f04928d58a93: N=3, CV=0.566%; sem-alerta-pela-triagem.
