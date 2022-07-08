# prometheus-grafana
Repositório acerca do curso de monitoramento de aplicações com Prometheus e Grafana


Tipos de Dados PromQL (Dados da linguagem de busca do Prometheus)

Vector: Vetor de séries temporais existentes
Ex.: busca por api_requests_total""
 - http_requests_total{method="POST", code="200"}
 - http_requests_total{method="POST", code="404"}
 - http_requests_total{method="POST", code="503"}

Scalar: número inteiro qualquer

Instant Vector: valores das séries temporais num determinado instante de tempo (timestamp)
- api_requests_total (@10/10/2021 22:59:00)

Range vector: Valor das séries temporais num intervalo de tempo
- api_requests_total[1m] (@10/10/2021 22:59:00)
- api_requests_total[4m:1m] (@10/10/2021 22:59:00) //4 minutos com intervalo de 1 minuto

Interpolação:
- api_requests_total[1m]