# Consolidação descritiva do piloto

Percentis por execução, sem pooling entre condições. Recursos permanecem diagnósticos, sem inferência de eficiência. Picos >=90 ms são um diagnóstico exploratório, não critério de exclusão.

| Etapa | Execução | Perfil | N | Erros | Média ms | Mediana | P95 | P99 | Corpo bytes | Queda entre metades % | Picos >=90 ms |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| P2 | netem0-pedidos-taxa20-m50-50-r1-bff | web | 3000 | 0 | 3.3447 | 3 | 4 | 5 | 1037.13 | 4.82 | 0 |
| P2 | netem0-pedidos-taxa20-m50-50-r1-bff | mobile | 3000 | 0 | 3.3413 | 3 | 4 | 5 | 217.89 | 4.79 | 0 |
| P2 | netem0-pedidos-taxa20-m50-50-r1-unificada | web | 3000 | 0 | 3.1647 | 3 | 4 | 4 | 1037.13 | -0.08 | 0 |
| P2 | netem0-pedidos-taxa20-m50-50-r1-unificada | mobile | 3000 | 0 | 3.1637 | 3 | 4 | 4 | 1037.13 | 0.23 | 0 |

## Variabilidade das médias entre execuções

- P2/bff/web: N=1; CV=indisponível. Três repetições não garantem precisão.
- P2/bff/mobile: N=1; CV=indisponível. Três repetições não garantem precisão.
- P2/unificada/web: N=1; CV=indisponível. Três repetições não garantem precisão.
- P2/unificada/mobile: N=1; CV=indisponível. Três repetições não garantem precisão.

## Recursos da entrada (diagnósticos)

Valores transcritos do consolidado de recursos: API ou soma dos dois BFFs por ciclo. CPU Docker não é método final validado; memória não é heap. Não comparar com cgroup de intervalo completo.

| Etapa | Execução | CPU média Docker % | Memória média MiB | Memória pico amostrado MiB |
| --- | --- | --- | --- | --- |
| P2 | netem0-pedidos-taxa20-m50-50-r1-bff | 8.243 | 575.34 | 579.70 |
| P2 | netem0-pedidos-taxa20-m50-50-r1-unificada | 5.852 | 372.63 | 393.30 |

Execuções excluídas/pendentes: 0. Detalhes, hashes, todas as camadas de recursos, gerador, blocos temporais e eventos por thread em analise.json.
