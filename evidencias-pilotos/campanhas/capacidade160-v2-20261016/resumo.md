# Consolidação descritiva do piloto

Percentis por execução, sem pooling entre condições. Recursos permanecem diagnósticos, sem inferência de eficiência. Picos >=90 ms são um diagnóstico exploratório, não critério de exclusão.

| Etapa | Execução | Perfil | N | Erros | Média ms | Mediana | P95 | P99 | Corpo bytes | Queda entre metades % | Picos >=90 ms |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Carga160v2 | netem0-pedidos-taxa160-m50-50-r1-bff | web | 24000 | 0 | 3.0749 | 3 | 4 | 4 | 1037.12 | 0.39 | 0 |
| Carga160v2 | netem0-pedidos-taxa160-m50-50-r1-bff | mobile | 24000 | 0 | 3.0605 | 3 | 4 | 4 | 217.89 | 0.44 | 0 |
| Carga160v2 | netem0-pedidos-taxa160-m50-50-r1-unificada | web | 24000 | 0 | 3.2099 | 3 | 4 | 5 | 1037.12 | 0.49 | 0 |
| Carga160v2 | netem0-pedidos-taxa160-m50-50-r1-unificada | mobile | 24000 | 0 | 3.2188 | 3 | 4 | 5 | 1037.12 | 0.37 | 0 |

## Variabilidade das médias entre execuções

- Carga160v2/bff/web: N=1; CV=indisponível. Três repetições não garantem precisão.
- Carga160v2/bff/mobile: N=1; CV=indisponível. Três repetições não garantem precisão.
- Carga160v2/unificada/web: N=1; CV=indisponível. Três repetições não garantem precisão.
- Carga160v2/unificada/mobile: N=1; CV=indisponível. Três repetições não garantem precisão.

## Recursos da entrada (diagnósticos)

Valores transcritos do consolidado de recursos: API ou soma dos dois BFFs por ciclo. CPU Docker não é método final validado; memória não é heap. Não comparar com cgroup de intervalo completo.

| Etapa | Execução | CPU média Docker % | Memória média MiB | Memória pico amostrado MiB |
| --- | --- | --- | --- | --- |
| Carga160v2 | netem0-pedidos-taxa160-m50-50-r1-bff | 49.110 | 575.69 | 577.30 |
| Carga160v2 | netem0-pedidos-taxa160-m50-50-r1-unificada | 46.616 | 375.08 | 395.70 |

Execuções excluídas/pendentes: 0. Detalhes, hashes, todas as camadas de recursos, gerador, blocos temporais e eventos por thread em analise.json.
