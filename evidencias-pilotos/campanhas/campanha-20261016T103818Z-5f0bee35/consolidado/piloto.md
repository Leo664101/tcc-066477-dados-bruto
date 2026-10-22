# Relatorio exploratorio do piloto

Criterios piloto v1: triagem heuristica, sem aprovar parametros oficiais. Ver piloto.json para valores, contagens e limites. Falhas tecnicas permanecem excluidas; falhas HTTP nao sao apagadas.

| Execucao | Perfil | Estado tecnico | Erros HTTP brutos da execucao | Aquecimento | Duracao |
| --- | --- | --- | --- | --- | --- |
| netem0-produtos-taxa20-m50-50-r1-bff | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-produtos-taxa20-m50-50-r1-bff | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-produtos-taxa20-m50-50-r1-unificada | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-produtos-taxa20-m50-50-r1-unificada | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |

## Variabilidade entre execucoes

- bff/mobile, condicao 1a52d380cf9cd2512c9b33c19e43a8f8bbd41978e45c5466e3bda525af8ad9e5: N=1, CV=indisponivel; dados-insuficientes.
- bff/web, condicao 1a52d380cf9cd2512c9b33c19e43a8f8bbd41978e45c5466e3bda525af8ad9e5: N=1, CV=indisponivel; dados-insuficientes.
- unificada/mobile, condicao 12500c1cab47817cdaf4dd2262fa3b849b3fcc28ae91eb22ae406111422f1d51: N=1, CV=indisponivel; dados-insuficientes.
- unificada/web, condicao 12500c1cab47817cdaf4dd2262fa3b849b3fcc28ae91eb22ae406111422f1d51: N=1, CV=indisponivel; dados-insuficientes.
