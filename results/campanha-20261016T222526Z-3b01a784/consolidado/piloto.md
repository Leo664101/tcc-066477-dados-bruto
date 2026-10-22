# Relatorio exploratorio do piloto

Criterios piloto v1: triagem heuristica, sem aprovar parametros oficiais. Ver piloto.json para valores, contagens e limites. Falhas tecnicas permanecem excluidas; falhas HTTP nao sao apagadas.

| Execucao | Perfil | Estado tecnico | Erros HTTP brutos da execucao | Aquecimento | Duracao |
| --- | --- | --- | --- | --- | --- |
| netem25-pedidos-taxa160-m50-50-r1-unificada | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem25-pedidos-taxa160-m50-50-r1-unificada | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem25-pedidos-taxa160-m50-50-r1-bff | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem25-pedidos-taxa160-m50-50-r1-bff | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |

## Variabilidade entre execucoes

- bff/mobile, condicao 4cb17f759540e8559408c41a6d42563722d1937fa131fb05044bef8835710bf3: N=1, CV=indisponivel; dados-insuficientes.
- bff/web, condicao 4cb17f759540e8559408c41a6d42563722d1937fa131fb05044bef8835710bf3: N=1, CV=indisponivel; dados-insuficientes.
- unificada/mobile, condicao 5d176b0251653bd0f06af941551e4981773e6374d9759257e2841da8ba121012: N=1, CV=indisponivel; dados-insuficientes.
- unificada/web, condicao 5d176b0251653bd0f06af941551e4981773e6374d9759257e2841da8ba121012: N=1, CV=indisponivel; dados-insuficientes.
