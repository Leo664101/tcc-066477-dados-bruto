# Relatorio exploratorio do piloto

Criterios piloto v1: triagem heuristica, sem aprovar parametros oficiais. Ver piloto.json para valores, contagens e limites. Falhas tecnicas permanecem excluidas; falhas HTTP nao sao apagadas.

| Execucao | Perfil | Estado tecnico | Erros HTTP brutos da execucao | Aquecimento | Duracao |
| --- | --- | --- | --- | --- | --- |
| netem0-produtos-taxa20-m50-50-r1-unificada | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-produtos-taxa20-m50-50-r1-unificada | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-produtos-taxa20-m50-50-r1-bff | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-produtos-taxa20-m50-50-r1-bff | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |

## Variabilidade entre execucoes

- bff/mobile, condicao 9b964df38b44084854760f14e536c05c5cbc8f3151cf826cc7c7de85c0a2483e: N=1, CV=indisponivel; dados-insuficientes.
- bff/web, condicao 9b964df38b44084854760f14e536c05c5cbc8f3151cf826cc7c7de85c0a2483e: N=1, CV=indisponivel; dados-insuficientes.
- unificada/mobile, condicao fa133b80644d3a61461604a7452acfa3c11d14ae5d02d033ba019fcf80b0b0c6: N=1, CV=indisponivel; dados-insuficientes.
- unificada/web, condicao fa133b80644d3a61461604a7452acfa3c11d14ae5d02d033ba019fcf80b0b0c6: N=1, CV=indisponivel; dados-insuficientes.
