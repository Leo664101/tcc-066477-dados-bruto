# Relatorio exploratorio do piloto

Criterios piloto v1: triagem heuristica, sem aprovar parametros oficiais. Ver piloto.json para valores, contagens e limites. Falhas tecnicas permanecem excluidas; falhas HTTP nao sao apagadas.

| Execucao | Perfil | Estado tecnico | Erros HTTP brutos da execucao | Aquecimento | Duracao |
| --- | --- | --- | --- | --- | --- |
| netem0-produtos-taxa20-m50-50-r1-unificada | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-produtos-taxa20-m50-50-r1-unificada | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-produtos-taxa20-m50-50-r1-bff | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-produtos-taxa20-m50-50-r1-bff | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |

## Variabilidade entre execucoes

- bff/mobile, condicao 49cb005af3a6e802527a85b107dbaeeb5939c1a612d2029fea744c26518a2c23: N=1, CV=indisponivel; dados-insuficientes.
- bff/web, condicao 49cb005af3a6e802527a85b107dbaeeb5939c1a612d2029fea744c26518a2c23: N=1, CV=indisponivel; dados-insuficientes.
- unificada/mobile, condicao ad2112611b0c8966c5b7ddc28eb7e3c878dde1a0a133ffcb2b1b95ce4a89bc15: N=1, CV=indisponivel; dados-insuficientes.
- unificada/web, condicao ad2112611b0c8966c5b7ddc28eb7e3c878dde1a0a133ffcb2b1b95ce4a89bc15: N=1, CV=indisponivel; dados-insuficientes.
