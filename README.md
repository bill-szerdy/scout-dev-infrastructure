# scout-dev-infrastructure
Spins up a Scout infrastructure

1. Call `docker-compose up -d`
2. Change directory to your Scout directory
3. Execute `rake config:seed` (only need to do this once)
4. Ready Player One..

This compose will spin up the following:


| Name        | Container               | Port                    |
| :---------: | :---------------------: | :---------------------: |
| PostgreSQL  | postgres:latest         | 5432 (needs work)       | 
| Redis       | redis:latest            | 6379                    |
| RabbitMQ    | rabbitme:3-management   | 4369, 5671-5672, 15672  |
| InfluxDB    | influxdb:latest         | 8086                    |
| Telegraf    | telegraf:latest         | 8092/udp                |
| Grafana     | grafana/grafana:latest  | 3000                    |

