# Consolidação descritiva do piloto

Percentis por execução, sem pooling entre condições. Recursos permanecem diagnósticos, sem inferência de eficiência. Picos >=90 ms são um diagnóstico exploratório, não critério de exclusão.

| Etapa | Execução | Perfil | N | Erros | Média ms | Mediana | P95 | P99 | Corpo bytes | Queda entre metades % | Picos >=90 ms |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Carga160rede25 | netem25-pedidos-taxa160-m50-50-r1-unificada | web | 24000 | 0 | 53.7418 | 53 | 54 | 60 | 1037.12 | 0.02 | 240 |
| Carga160rede25 | netem25-pedidos-taxa160-m50-50-r1-unificada | mobile | 24000 | 0 | 53.7392 | 53 | 54 | 60 | 1037.12 | 0.04 | 240 |
| Carga160rede25 | netem25-pedidos-taxa160-m50-50-r1-bff | web | 24000 | 0 | 53.6590 | 53 | 54 | 77 | 1037.12 | -0.00 | 240 |
| Carga160rede25 | netem25-pedidos-taxa160-m50-50-r1-bff | mobile | 24000 | 0 | 53.6373 | 53 | 54 | 61 | 217.89 | 0.01 | 240 |

## Variabilidade das médias entre execuções

- Carga160rede25/unificada/web: N=1; CV=indisponível. Três repetições não garantem precisão.
- Carga160rede25/unificada/mobile: N=1; CV=indisponível. Três repetições não garantem precisão.
- Carga160rede25/bff/web: N=1; CV=indisponível. Três repetições não garantem precisão.
- Carga160rede25/bff/mobile: N=1; CV=indisponível. Três repetições não garantem precisão.

## Recursos da entrada (diagnósticos)

Valores transcritos do consolidado de recursos: API ou soma dos dois BFFs por ciclo. CPU Docker não é método final validado; memória não é heap. Não comparar com cgroup de intervalo completo.

| Etapa | Execução | CPU média Docker % | Memória média MiB | Memória pico amostrado MiB |
| --- | --- | --- | --- | --- |
| Carga160rede25 | netem25-pedidos-taxa160-m50-50-r1-unificada | 46.160 | 379.04 | 393.70 |
| Carga160rede25 | netem25-pedidos-taxa160-m50-50-r1-bff | 49.454 | 592.14 | 593.50 |

Execuções excluídas/pendentes: 0. Detalhes, hashes, todas as camadas de recursos, gerador, blocos temporais e eventos por thread em analise.json.
