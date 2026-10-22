# Relatorio exploratorio do piloto

Criterios piloto v1: triagem heuristica, sem aprovar parametros oficiais. Ver piloto.json para valores, contagens e limites. Falhas tecnicas permanecem excluidas; falhas HTTP nao sao apagadas.

| Execucao | Perfil | Estado tecnico | Erros HTTP brutos da execucao | Aquecimento | Duracao |
| --- | --- | --- | --- | --- | --- |
| netem0-pedidos-taxa20-m50-50-r1-bff | web | incluida | 0 | nao-confirmado | sem-alerta-pela-triagem |
| netem0-pedidos-taxa20-m50-50-r1-bff | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa20-m50-50-r1-unificada | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa20-m50-50-r1-unificada | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |

## Variabilidade entre execucoes

- bff/mobile, condicao c90725060b5121a9951c0be4731dc7527ea23963631bf608c88754ac0590bd92: N=1, CV=indisponivel; dados-insuficientes.
- bff/web, condicao c90725060b5121a9951c0be4731dc7527ea23963631bf608c88754ac0590bd92: N=1, CV=indisponivel; dados-insuficientes.
- unificada/mobile, condicao c4fafb3329a8de3a3a943dbdf1dffe8f86031852ce68e485183fe03fd66dadd7: N=1, CV=indisponivel; dados-insuficientes.
- unificada/web, condicao c4fafb3329a8de3a3a943dbdf1dffe8f86031852ce68e485183fe03fd66dadd7: N=1, CV=indisponivel; dados-insuficientes.
