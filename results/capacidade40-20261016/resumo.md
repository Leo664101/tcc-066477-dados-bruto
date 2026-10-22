# Consolidação descritiva do piloto

Percentis por execução, sem pooling entre condições. Recursos permanecem diagnósticos, sem inferência de eficiência. Picos >=90 ms são um diagnóstico exploratório, não critério de exclusão.

| Etapa | Execução | Perfil | N | Erros | Média ms | Mediana | P95 | P99 | Corpo bytes | Queda entre metades % | Picos >=90 ms |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Carga40 | netem0-pedidos-taxa40-m50-50-r1-bff | web | 6000 | 0 | 3.1920 | 3 | 4 | 4 | 1037.13 | 1.57 | 0 |
| Carga40 | netem0-pedidos-taxa40-m50-50-r1-bff | mobile | 6000 | 0 | 3.1843 | 3 | 4 | 4 | 217.89 | 1.64 | 0 |
| Carga40 | netem0-pedidos-taxa40-m50-50-r1-unificada | web | 6000 | 0 | 3.2203 | 3 | 4 | 5 | 1037.13 | -0.23 | 0 |
| Carga40 | netem0-pedidos-taxa40-m50-50-r1-unificada | mobile | 6000 | 0 | 3.2197 | 3 | 4 | 5 | 1037.13 | -0.08 | 0 |

## Variabilidade das médias entre execuções

- Carga40/bff/web: N=1; CV=indisponível. Três repetições não garantem precisão.
- Carga40/bff/mobile: N=1; CV=indisponível. Três repetições não garantem precisão.
- Carga40/unificada/web: N=1; CV=indisponível. Três repetições não garantem precisão.
- Carga40/unificada/mobile: N=1; CV=indisponível. Três repetições não garantem precisão.

## Recursos da entrada (diagnósticos)

Valores transcritos do consolidado de recursos: API ou soma dos dois BFFs por ciclo. CPU Docker não é método final validado; memória não é heap. Não comparar com cgroup de intervalo completo.

| Etapa | Execução | CPU média Docker % | Memória média MiB | Memória pico amostrado MiB |
| --- | --- | --- | --- | --- |
| Carga40 | netem0-pedidos-taxa40-m50-50-r1-bff | 13.938 | 577.69 | 579.10 |
| Carga40 | netem0-pedidos-taxa40-m50-50-r1-unificada | 12.559 | 364.37 | 384.70 |

Execuções excluídas/pendentes: 0. Detalhes, hashes, todas as camadas de recursos, gerador, blocos temporais e eventos por thread em analise.json.
