# Consolidação descritiva do piloto

Percentis por execução, sem pooling entre condições. Recursos permanecem diagnósticos, sem inferência de eficiência. Picos >=90 ms são um diagnóstico exploratório, não critério de exclusão.

| Etapa | Execução | Perfil | N | Erros | Média ms | Mediana | P95 | P99 | Corpo bytes | Queda entre metades % | Picos >=90 ms |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| A | netem0-pedidos-taxa20-m50-50-r1-unificada | web | 3000 | 0 | 3.9617 | 4 | 5 | 5 | 1037.10 | 18.49 | 0 |
| A | netem0-pedidos-taxa20-m50-50-r1-unificada | mobile | 3000 | 0 | 3.9603 | 4 | 5 | 5 | 1037.10 | 18.53 | 0 |
| A | netem0-pedidos-taxa20-m50-50-r1-bff | web | 3000 | 0 | 4.1290 | 4 | 5 | 6 | 1037.10 | 16.79 | 0 |
| A | netem0-pedidos-taxa20-m50-50-r1-bff | mobile | 3000 | 0 | 4.1187 | 4 | 5 | 6 | 217.88 | 16.76 | 0 |
| A | netem0-pedidos-taxa20-m50-50-r2-bff | web | 3000 | 0 | 4.1307 | 4 | 5 | 6 | 1037.10 | 16.93 | 0 |
| A | netem0-pedidos-taxa20-m50-50-r2-bff | mobile | 3000 | 0 | 4.1203 | 4 | 5 | 6 | 217.88 | 17.17 | 0 |
| A | netem0-pedidos-taxa20-m50-50-r2-unificada | web | 3000 | 0 | 3.9260 | 4 | 5 | 5 | 1037.10 | 19.05 | 0 |
| A | netem0-pedidos-taxa20-m50-50-r2-unificada | mobile | 3000 | 0 | 3.9217 | 4 | 5 | 5 | 1037.10 | 18.78 | 0 |
| A | netem0-pedidos-taxa20-m50-50-r3-unificada | web | 3000 | 0 | 3.9207 | 4 | 5 | 5 | 1037.10 | 18.71 | 0 |
| A | netem0-pedidos-taxa20-m50-50-r3-unificada | mobile | 3000 | 0 | 3.9300 | 4 | 5 | 5 | 1037.10 | 18.59 | 0 |
| A | netem0-pedidos-taxa20-m50-50-r3-bff | web | 3000 | 0 | 4.1257 | 4 | 5 | 6 | 1037.10 | 17.66 | 0 |
| A | netem0-pedidos-taxa20-m50-50-r3-bff | mobile | 3000 | 0 | 4.1157 | 4 | 5 | 6 | 217.88 | 17.86 | 0 |
| B1 | netem0-produtos-taxa20-m50-50-r1-bff | web | 3000 | 0 | 2.7080 | 3 | 4 | 4 | 177.87 | 18.46 | 0 |
| B1 | netem0-produtos-taxa20-m50-50-r1-bff | mobile | 3000 | 0 | 2.7093 | 3 | 4 | 4 | 177.87 | 18.37 | 0 |
| B1 | netem0-produtos-taxa20-m50-50-r1-unificada | web | 3000 | 0 | 2.4060 | 2 | 3 | 4 | 177.87 | 21.73 | 0 |
| B1 | netem0-produtos-taxa20-m50-50-r1-unificada | mobile | 3000 | 0 | 2.4047 | 2 | 3 | 4 | 177.87 | 22.40 | 0 |
| B2 | netem25-pedidos-taxa20-m50-50-r1-unificada | web | 3000 | 0 | 54.7913 | 54 | 55 | 105 | 1037.10 | 1.15 | 40 |
| B2 | netem25-pedidos-taxa20-m50-50-r1-unificada | mobile | 3000 | 0 | 54.7997 | 54 | 55 | 105 | 1037.10 | 1.17 | 40 |
| B2 | netem25-pedidos-taxa20-m50-50-r1-bff | web | 3000 | 0 | 55.0717 | 54 | 55 | 105 | 1037.10 | 0.96 | 40 |
| B2 | netem25-pedidos-taxa20-m50-50-r1-bff | mobile | 3000 | 0 | 55.0807 | 54 | 55 | 105 | 217.88 | 0.95 | 40 |
| B3 | netem25-pedidos-taxa40-m50-50-r1-bff | web | 6000 | 0 | 53.9525 | 53 | 54 | 62 | 1037.10 | 0.95 | 57 |
| B3 | netem25-pedidos-taxa40-m50-50-r1-bff | mobile | 6000 | 0 | 53.9488 | 53 | 54 | 62 | 217.89 | 0.96 | 57 |
| B3 | netem25-pedidos-taxa40-m50-50-r1-unificada | web | 6000 | 0 | 53.8022 | 53 | 54 | 60 | 1037.10 | 0.50 | 56 |
| B3 | netem25-pedidos-taxa40-m50-50-r1-unificada | mobile | 6000 | 0 | 53.8077 | 53 | 54 | 60 | 1037.10 | 0.50 | 56 |

## Variabilidade das médias entre execuções

- A/unificada/web: N=3; CV=0.566%. Três repetições não garantem precisão.
- A/unificada/mobile: N=3; CV=0.517%. Três repetições não garantem precisão.
- A/bff/web: N=3; CV=0.062%. Três repetições não garantem precisão.
- A/bff/mobile: N=3; CV=0.057%. Três repetições não garantem precisão.
- B1/bff/web: N=1; CV=indisponível. Três repetições não garantem precisão.
- B1/bff/mobile: N=1; CV=indisponível. Três repetições não garantem precisão.
- B1/unificada/web: N=1; CV=indisponível. Três repetições não garantem precisão.
- B1/unificada/mobile: N=1; CV=indisponível. Três repetições não garantem precisão.
- B2/unificada/web: N=1; CV=indisponível. Três repetições não garantem precisão.
- B2/unificada/mobile: N=1; CV=indisponível. Três repetições não garantem precisão.
- B2/bff/web: N=1; CV=indisponível. Três repetições não garantem precisão.
- B2/bff/mobile: N=1; CV=indisponível. Três repetições não garantem precisão.
- B3/bff/web: N=1; CV=indisponível. Três repetições não garantem precisão.
- B3/bff/mobile: N=1; CV=indisponível. Três repetições não garantem precisão.
- B3/unificada/web: N=1; CV=indisponível. Três repetições não garantem precisão.
- B3/unificada/mobile: N=1; CV=indisponível. Três repetições não garantem precisão.

## Recursos da entrada (diagnósticos)

Valores transcritos do consolidado de recursos: API ou soma dos dois BFFs por ciclo. CPU Docker não é método final validado; memória não é heap. Não comparar com cgroup de intervalo completo.

| Etapa | Execução | CPU média Docker % | Memória média MiB | Memória pico amostrado MiB |
| --- | --- | --- | --- | --- |
| A | netem0-pedidos-taxa20-m50-50-r1-unificada | 7.414 | 362.93 | 383.30 |
| A | netem0-pedidos-taxa20-m50-50-r1-bff | 10.979 | 566.46 | 586.70 |
| A | netem0-pedidos-taxa20-m50-50-r2-bff | 11.041 | 531.86 | 542.10 |
| A | netem0-pedidos-taxa20-m50-50-r2-unificada | 7.498 | 340.83 | 361.80 |
| A | netem0-pedidos-taxa20-m50-50-r3-unificada | 7.521 | 346.18 | 365.00 |
| A | netem0-pedidos-taxa20-m50-50-r3-bff | 11.040 | 518.94 | 553.10 |
| B1 | netem0-produtos-taxa20-m50-50-r1-bff | 6.264 | 537.08 | 553.70 |
| B1 | netem0-produtos-taxa20-m50-50-r1-unificada | 4.803 | 355.91 | 364.10 |
| B2 | netem25-pedidos-taxa20-m50-50-r1-unificada | 7.339 | 359.44 | 365.20 |
| B2 | netem25-pedidos-taxa20-m50-50-r1-bff | 10.843 | 554.59 | 583.20 |
| B3 | netem25-pedidos-taxa40-m50-50-r1-bff | 15.933 | 567.63 | 609.30 |
| B3 | netem25-pedidos-taxa40-m50-50-r1-unificada | 12.793 | 369.33 | 371.00 |

Execuções excluídas/pendentes: 0. Detalhes, hashes, todas as camadas de recursos, gerador, blocos temporais e eventos por thread em analise.json.
