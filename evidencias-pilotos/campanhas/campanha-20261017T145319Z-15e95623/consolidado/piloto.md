# Relatorio exploratorio do piloto

Criterios piloto v1: triagem heuristica, sem aprovar parametros oficiais. Ver piloto.json para valores, contagens e limites. Falhas tecnicas permanecem excluidas; falhas HTTP nao sao apagadas.

| Execucao | Perfil | Estado tecnico | Erros HTTP brutos da execucao | Aquecimento | Duracao |
| --- | --- | --- | --- | --- | --- |
| netem25-pedidos-taxa160-m50-50-r1-bff | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem25-pedidos-taxa160-m50-50-r1-bff | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem25-pedidos-taxa160-m50-50-r1-unificada | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem25-pedidos-taxa160-m50-50-r1-unificada | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |

## Variabilidade entre execucoes

- bff/mobile, condicao 15cb1a88b5f3f161584628471f695e336eeb1e686b12d9f1fe23ea247c751fbe: N=1, CV=indisponivel; dados-insuficientes.
- bff/web, condicao 15cb1a88b5f3f161584628471f695e336eeb1e686b12d9f1fe23ea247c751fbe: N=1, CV=indisponivel; dados-insuficientes.
- unificada/mobile, condicao 0f97d37b9d2682c5f19be045f50a4fcaef0860d16da878bd5348afba4b25d357: N=1, CV=indisponivel; dados-insuficientes.
- unificada/web, condicao 0f97d37b9d2682c5f19be045f50a4fcaef0860d16da878bd5348afba4b25d357: N=1, CV=indisponivel; dados-insuficientes.
