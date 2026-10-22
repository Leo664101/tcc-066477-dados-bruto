# Consolidação descritiva do piloto

Percentis por execução, sem pooling entre condições. Recursos permanecem diagnósticos, sem inferência de eficiência. Picos >=90 ms são um diagnóstico exploratório, não critério de exclusão.

| Etapa | Execução | Perfil | N | Erros | Média ms | Mediana | P95 | P99 | Corpo bytes | Queda entre metades % | Picos >=90 ms |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| CPU1 | netem25-pedidos-taxa160-m50-50-r1-bff | web | 24001 | 0 | 53.3375 | 53 | 54 | 72 | 1037.10 | -0.03 | 240 |
| CPU1 | netem25-pedidos-taxa160-m50-50-r1-bff | mobile | 24001 | 0 | 53.3213 | 53 | 54 | 61 | 217.88 | -0.01 | 240 |
| CPU1 | netem25-pedidos-taxa160-m50-50-r1-unificada | web | 24000 | 0 | 53.4385 | 53 | 54 | 62 | 1037.12 | 0.04 | 240 |
| CPU1 | netem25-pedidos-taxa160-m50-50-r1-unificada | mobile | 24000 | 0 | 53.4369 | 53 | 54 | 62 | 1037.12 | 0.04 | 240 |

## Variabilidade das médias entre execuções

- CPU1/bff/web: N=1; CV=indisponível. Três repetições não garantem precisão.
- CPU1/bff/mobile: N=1; CV=indisponível. Três repetições não garantem precisão.
- CPU1/unificada/web: N=1; CV=indisponível. Três repetições não garantem precisão.
- CPU1/unificada/mobile: N=1; CV=indisponível. Três repetições não garantem precisão.

## Recursos da entrada (diagnósticos)

Valores transcritos do consolidado de recursos: API ou soma dos dois BFFs por ciclo. CPU Docker não é método final validado; memória não é heap. Não comparar com cgroup de intervalo completo.

| Etapa | Execução | CPU média Docker % | Memória média MiB | Memória pico amostrado MiB |
| --- | --- | --- | --- | --- |
| CPU1 | netem25-pedidos-taxa160-m50-50-r1-bff | 43.855 | 584.97 | 587.40 |
| CPU1 | netem25-pedidos-taxa160-m50-50-r1-unificada | 41.231 | 370.33 | 388.40 |

Execuções excluídas/pendentes: 0. Detalhes, hashes, todas as camadas de recursos, gerador, blocos temporais e eventos por thread em analise.json.
