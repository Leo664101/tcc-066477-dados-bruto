# Relatorio exploratorio do piloto

Criterios piloto v1: triagem heuristica, sem aprovar parametros oficiais. Ver piloto.json para valores, contagens e limites. Falhas tecnicas permanecem excluidas; falhas HTTP nao sao apagadas.

| Execucao | Perfil | Estado tecnico | Erros HTTP brutos da execucao | Aquecimento | Duracao |
| --- | --- | --- | --- | --- | --- |
| netem25-pedidos-taxa20-m50-50-r1-unificada | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem25-pedidos-taxa20-m50-50-r1-unificada | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem25-pedidos-taxa20-m50-50-r1-bff | web | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |
| netem25-pedidos-taxa20-m50-50-r1-bff | mobile | incluida | 0 | confirmado-pela-triagem | sem-alerta-pela-triagem |

## Variabilidade entre execucoes

- bff/mobile, condicao 0e90727c81f35529264ec07b989b652d05e23e23398b07cf96fcb6d35a9d5572: N=1, CV=indisponivel; dados-insuficientes.
- bff/web, condicao 0e90727c81f35529264ec07b989b652d05e23e23398b07cf96fcb6d35a9d5572: N=1, CV=indisponivel; dados-insuficientes.
- unificada/mobile, condicao 0d3e9fbf72567ef6943d53db14fe87af4f6d29d245ba74aa11053b98a429186b: N=1, CV=indisponivel; dados-insuficientes.
- unificada/web, condicao 0d3e9fbf72567ef6943d53db14fe87af4f6d29d245ba74aa11053b98a429186b: N=1, CV=indisponivel; dados-insuficientes.
