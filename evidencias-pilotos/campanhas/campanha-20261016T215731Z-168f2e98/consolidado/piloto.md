# Relatorio exploratorio do piloto

Criterios piloto v1: triagem heuristica, sem aprovar parametros oficiais. Ver piloto.json para valores, contagens e limites. Falhas tecnicas permanecem excluidas; falhas HTTP nao sao apagadas.

| Execucao | Perfil | Estado tecnico | Erros HTTP brutos da execucao | Aquecimento | Duracao |
| --- | --- | --- | --- | --- | --- |
| netem0-pedidos-taxa160-m50-50-r1-bff | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa160-m50-50-r1-bff | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa160-m50-50-r1-unificada | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa160-m50-50-r1-unificada | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |

## Variabilidade entre execucoes

- bff/mobile, condicao 7f52bccbeff6388463a2c41ff2f9eb0d58788db39fb5e0f248ecedcc63a625e4: N=1, CV=indisponivel; dados-insuficientes.
- bff/web, condicao 7f52bccbeff6388463a2c41ff2f9eb0d58788db39fb5e0f248ecedcc63a625e4: N=1, CV=indisponivel; dados-insuficientes.
- unificada/mobile, condicao 16a9b7622a452f962e76cbd8b0f5f50fed6e2d145ccd43087110834fdebd8730: N=1, CV=indisponivel; dados-insuficientes.
- unificada/web, condicao 16a9b7622a452f962e76cbd8b0f5f50fed6e2d145ccd43087110834fdebd8730: N=1, CV=indisponivel; dados-insuficientes.
