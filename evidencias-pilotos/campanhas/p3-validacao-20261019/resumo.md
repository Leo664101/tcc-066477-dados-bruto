# Consolidação descritiva do piloto

Percentis por execução, sem pooling entre condições. Recursos permanecem diagnósticos, sem inferência de eficiência. Picos >=90 ms são um diagnóstico exploratório, não critério de exclusão.

| Etapa | Execução | Perfil | N | Erros | Média ms | Mediana | P95 | P99 | Corpo bytes | Queda entre metades % | Picos >=90 ms |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| P3 | netem0-pedidos-taxa160-m50-50-r1-unificada | web | 24000 | 0 | 2.9223 | 3 | 4 | 4 | 1037.12 | 0.14 | 0 |
| P3 | netem0-pedidos-taxa160-m50-50-r1-unificada | mobile | 24000 | 0 | 2.9200 | 3 | 4 | 4 | 1037.12 | 0.43 | 0 |
| P3 | netem0-pedidos-taxa160-m50-50-r1-bff | web | 24000 | 0 | 2.7886 | 3 | 4 | 4 | 1037.12 | 1.14 | 0 |
| P3 | netem0-pedidos-taxa160-m50-50-r1-bff | mobile | 24000 | 0 | 2.7794 | 3 | 4 | 4 | 217.89 | 0.76 | 0 |

## Variabilidade das médias entre execuções

- P3/unificada/web: N=1; CV=indisponível. Três repetições não garantem precisão.
- P3/unificada/mobile: N=1; CV=indisponível. Três repetições não garantem precisão.
- P3/bff/web: N=1; CV=indisponível. Três repetições não garantem precisão.
- P3/bff/mobile: N=1; CV=indisponível. Três repetições não garantem precisão.

## Recursos da entrada (diagnósticos)

Valores transcritos do consolidado de recursos: API ou soma dos dois BFFs por ciclo. CPU Docker não é método final validado; memória não é heap. Não comparar com cgroup de intervalo completo.

| Etapa | Execução | CPU média Docker % | Memória média MiB | Memória pico amostrado MiB |
| --- | --- | --- | --- | --- |
| P3 | netem0-pedidos-taxa160-m50-50-r1-unificada | 41.508 | 376.00 | 377.00 |
| P3 | netem0-pedidos-taxa160-m50-50-r1-bff | 44.059 | 586.24 | 605.90 |

Execuções excluídas/pendentes: 0. Detalhes, hashes, todas as camadas de recursos, gerador, blocos temporais e eventos por thread em analise.json.
