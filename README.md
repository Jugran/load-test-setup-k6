# docker-k6-grafana-influxdb
Demonstrates how to run load tests with containerised instances of K6, Grafana and InfluxDB.
https://github.com/luketn/docker-k6-grafana-influxdb



## Usage
1. Run monitoring containers first
   ```sh
    docker compose --profile monitoring up -d
   ```
2. Configure start script to run by k6 in docker-compose.yml
3. Run the k6 container for load testing
   ```sh
    docker compose run --rm k6
   ```

Load testing results can be viewed in Grafana at http://localhost:3000/d/k6/k6-load-testing-results