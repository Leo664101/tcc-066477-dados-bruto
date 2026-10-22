# Relatorio exploratorio do piloto

Criterios piloto v1: triagem heuristica, sem aprovar parametros oficiais. Ver piloto.json para valores, contagens e limites. Falhas tecnicas permanecem excluidas; falhas HTTP nao sao apagadas.

| Execucao | Perfil | Estado tecnico | Erros HTTP brutos da execucao | Aquecimento | Duracao |
| --- | --- | --- | --- | --- | --- |
| netem0-produtos-taxa20-m50-50-r1-unificada | web | incluida | 0 | dados-insuficientes | dados-insuficientes |
| netem0-produtos-taxa20-m50-50-r1-unificada | mobile | incluida | 0 | dados-insuficientes | dados-insuficientes |
| netem0-produtos-taxa20-m50-50-r1-bff | web | incluida | 0 | dados-insuficientes | dados-insuficientes |
| netem0-produtos-taxa20-m50-50-r1-bff | mobile | incluida | 0 | dados-insuficientes | dados-insuficientes |

## Variabilidade entre execucoes

- bff/mobile, condicao e9539384be74674d344a94cb491ceb58fce100a550bab900bf001c6a144f9c79: N=1, CV=indisponivel; dados-insuficientes.
- bff/web, condicao e9539384be74674d344a94cb491ceb58fce100a550bab900bf001c6a144f9c79: N=1, CV=indisponivel; dados-insuficientes.
- unificada/mobile, condicao 9e84ecb1f39e8e057de8c9c284ab87a3f8740d7dfe276ef8ae81b86966ee8c91: N=1, CV=indisponivel; dados-insuficientes.
- unificada/web, condicao 9e84ecb1f39e8e057de8c9c284ab87a3f8740d7dfe276ef8ae81b86966ee8c91: N=1, CV=indisponivel; dados-insuficientes.
