# Relatorio exploratorio do piloto

Criterios piloto v1: triagem heuristica, sem aprovar parametros oficiais. Ver piloto.json para valores, contagens e limites. Falhas tecnicas permanecem excluidas; falhas HTTP nao sao apagadas.

| Execucao | Perfil | Estado tecnico | Erros HTTP brutos da execucao | Aquecimento | Duracao |
| --- | --- | --- | --- | --- | --- |
| netem0-pedidos-taxa20-m50-50-r1-unificada | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa20-m50-50-r1-unificada | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa20-m50-50-r1-bff | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa20-m50-50-r1-bff | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |

## Variabilidade entre execucoes

- bff/mobile, condicao cb37228fe4dc98b0ebd0127146e86c341efcaaf7c7dc3d6b17fa7006ac2438e2: N=1, CV=indisponivel; dados-insuficientes.
- bff/web, condicao cb37228fe4dc98b0ebd0127146e86c341efcaaf7c7dc3d6b17fa7006ac2438e2: N=1, CV=indisponivel; dados-insuficientes.
- unificada/mobile, condicao 7f083d1e42722e647d43457896c07aae3575c40b2e709c0e37b48c303759fd17: N=1, CV=indisponivel; dados-insuficientes.
- unificada/web, condicao 7f083d1e42722e647d43457896c07aae3575c40b2e709c0e37b48c303759fd17: N=1, CV=indisponivel; dados-insuficientes.
