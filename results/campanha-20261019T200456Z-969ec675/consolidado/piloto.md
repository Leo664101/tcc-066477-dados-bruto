# Relatorio exploratorio do piloto

Criterios piloto v1: triagem heuristica, sem aprovar parametros oficiais. Ver piloto.json para valores, contagens e limites. Falhas tecnicas permanecem excluidas; falhas HTTP nao sao apagadas.

| Execucao | Perfil | Estado tecnico | Erros HTTP brutos da execucao | Aquecimento | Duracao |
| --- | --- | --- | --- | --- | --- |
| netem0-pedidos-taxa160-m50-50-r1-bff | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa160-m50-50-r1-bff | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa160-m50-50-r1-unificada | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem0-pedidos-taxa160-m50-50-r1-unificada | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |

## Variabilidade entre execucoes

- bff/mobile, condicao a72ac3c9b331c07162aa49d58a3631074503bd112a57cd6eee27b73724664e46: N=1, CV=indisponivel; dados-insuficientes.
- bff/web, condicao a72ac3c9b331c07162aa49d58a3631074503bd112a57cd6eee27b73724664e46: N=1, CV=indisponivel; dados-insuficientes.
- unificada/mobile, condicao 90dd80a7ac2e65d478b2060cfe8145ea79cb6e34c6e585a0157de65fd284649b: N=1, CV=indisponivel; dados-insuficientes.
- unificada/web, condicao 90dd80a7ac2e65d478b2060cfe8145ea79cb6e34c6e585a0157de65fd284649b: N=1, CV=indisponivel; dados-insuficientes.
