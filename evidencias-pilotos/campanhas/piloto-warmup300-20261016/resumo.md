# Consolidação descritiva do piloto

Percentis por execução, sem pooling entre condições. Recursos permanecem diagnósticos, sem inferência de eficiência. Picos >=90 ms são um diagnóstico exploratório, não critério de exclusão.

| Etapa | Execução | Perfil | N | Erros | Média ms | Mediana | P95 | P99 | Corpo bytes | Queda entre metades % | Picos >=90 ms |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| W300 | netem0-pedidos-taxa20-m50-50-r1-unificada | web | 3000 | 0 | 3.3733 | 3 | 4 | 5 | 1037.13 | -0.20 | 0 |
| W300 | netem0-pedidos-taxa20-m50-50-r1-unificada | mobile | 3000 | 0 | 3.3713 | 3 | 4 | 5 | 1037.13 | 0.39 | 0 |
| W300 | netem0-pedidos-taxa20-m50-50-r1-bff | web | 3000 | 0 | 3.5147 | 3 | 4 | 5 | 1037.13 | 3.54 | 0 |
| W300 | netem0-pedidos-taxa20-m50-50-r1-bff | mobile | 3000 | 0 | 3.5127 | 3 | 4 | 5 | 217.89 | 3.54 | 0 |

## Variabilidade das médias entre execuções

- W300/unificada/web: N=1; CV=indisponível. Três repetições não garantem precisão.
- W300/unificada/mobile: N=1; CV=indisponível. Três repetições não garantem precisão.
- W300/bff/web: N=1; CV=indisponível. Três repetições não garantem precisão.
- W300/bff/mobile: N=1; CV=indisponível. Três repetições não garantem precisão.

## Recursos da entrada (diagnósticos)

Valores transcritos do consolidado de recursos: API ou soma dos dois BFFs por ciclo. CPU Docker não é método final validado; memória não é heap. Não comparar com cgroup de intervalo completo.

| Etapa | Execução | CPU média Docker % | Memória média MiB | Memória pico amostrado MiB |
| --- | --- | --- | --- | --- |
| W300 | netem0-pedidos-taxa20-m50-50-r1-unificada | 6.529 | 362.25 | 363.10 |
| W300 | netem0-pedidos-taxa20-m50-50-r1-bff | 9.153 | 571.51 | 576.40 |

Execuções excluídas/pendentes: 0. Detalhes, hashes, todas as camadas de recursos, gerador, blocos temporais e eventos por thread em analise.json.
