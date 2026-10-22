# Consolidação descritiva do piloto

Percentis por execução, sem pooling entre condições. Recursos permanecem diagnósticos, sem inferência de eficiência. Picos >=90 ms são um diagnóstico exploratório, não critério de exclusão.

| Etapa | Execução | Perfil | N | Erros | Média ms | Mediana | P95 | P99 | Corpo bytes | Queda entre metades % | Picos >=90 ms |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| P1 | netem0-produtos-taxa20-m50-50-r1-unificada | web | 3000 | 0 | 1.9213 | 2 | 3 | 3 | 177.87 | 1.45 | 0 |
| P1 | netem0-produtos-taxa20-m50-50-r1-unificada | mobile | 3000 | 0 | 1.9237 | 2 | 3 | 3 | 177.87 | 0.52 | 0 |
| P1 | netem0-produtos-taxa20-m50-50-r1-bff | web | 3000 | 0 | 2.2077 | 2 | 3 | 3 | 177.87 | 4.05 | 0 |
| P1 | netem0-produtos-taxa20-m50-50-r1-bff | mobile | 3000 | 0 | 2.2003 | 2 | 3 | 3 | 177.87 | 4.53 | 0 |

## Variabilidade das médias entre execuções

- P1/unificada/web: N=1; CV=indisponível. Três repetições não garantem precisão.
- P1/unificada/mobile: N=1; CV=indisponível. Três repetições não garantem precisão.
- P1/bff/web: N=1; CV=indisponível. Três repetições não garantem precisão.
- P1/bff/mobile: N=1; CV=indisponível. Três repetições não garantem precisão.

## Recursos da entrada (diagnósticos)

Valores transcritos do consolidado de recursos: API ou soma dos dois BFFs por ciclo. CPU Docker não é método final validado; memória não é heap. Não comparar com cgroup de intervalo completo.

| Etapa | Execução | CPU média Docker % | Memória média MiB | Memória pico amostrado MiB |
| --- | --- | --- | --- | --- |
| P1 | netem0-produtos-taxa20-m50-50-r1-unificada | 2.690 | 359.36 | 381.70 |
| P1 | netem0-produtos-taxa20-m50-50-r1-bff | 5.254 | 561.15 | 596.10 |

Execuções excluídas/pendentes: 0. Detalhes, hashes, todas as camadas de recursos, gerador, blocos temporais e eventos por thread em analise.json.
