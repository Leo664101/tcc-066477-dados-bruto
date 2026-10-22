# Consolidação descritiva do piloto

Percentis por execução, sem pooling entre condições. Recursos permanecem diagnósticos, sem inferência de eficiência. Picos >=90 ms são um diagnóstico exploratório, não critério de exclusão.

| Etapa | Execução | Perfil | N | Erros | Média ms | Mediana | P95 | P99 | Corpo bytes | Queda entre metades % | Picos >=90 ms |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Carga80v2 | netem0-pedidos-taxa80-m50-50-r1-unificada | web | 12000 | 0 | 3.0996 | 3 | 4 | 4 | 1037.12 | 0.46 | 0 |
| Carga80v2 | netem0-pedidos-taxa80-m50-50-r1-unificada | mobile | 12000 | 0 | 3.0962 | 3 | 4 | 4 | 1037.12 | 0.67 | 0 |
| Carga80v2 | netem0-pedidos-taxa80-m50-50-r1-bff | web | 12000 | 0 | 3.0435 | 3 | 4 | 4 | 1037.12 | 0.25 | 0 |
| Carga80v2 | netem0-pedidos-taxa80-m50-50-r1-bff | mobile | 12000 | 0 | 3.0357 | 3 | 4 | 4 | 217.89 | 0.46 | 0 |

## Variabilidade das médias entre execuções

- Carga80v2/unificada/web: N=1; CV=indisponível. Três repetições não garantem precisão.
- Carga80v2/unificada/mobile: N=1; CV=indisponível. Três repetições não garantem precisão.
- Carga80v2/bff/web: N=1; CV=indisponível. Três repetições não garantem precisão.
- Carga80v2/bff/mobile: N=1; CV=indisponível. Três repetições não garantem precisão.

## Recursos da entrada (diagnósticos)

Valores transcritos do consolidado de recursos: API ou soma dos dois BFFs por ciclo. CPU Docker não é método final validado; memória não é heap. Não comparar com cgroup de intervalo completo.

| Etapa | Execução | CPU média Docker % | Memória média MiB | Memória pico amostrado MiB |
| --- | --- | --- | --- | --- |
| Carga80v2 | netem0-pedidos-taxa80-m50-50-r1-unificada | 24.217 | 371.13 | 372.40 |
| Carga80v2 | netem0-pedidos-taxa80-m50-50-r1-bff | 26.426 | 576.04 | 580.00 |

Execuções excluídas/pendentes: 0. Detalhes, hashes, todas as camadas de recursos, gerador, blocos temporais e eventos por thread em analise.json.
