# re:doubt data-platform

## ETL

ETL based on Airflow. Jobs list:

* [rebuild-top-jettons-datamart](etl/dags/rebuild-top-jettons-datamart.py) - creates datamart with top jettons by market volume
* [TON Rocket indexer](etl/dags/ton_rocket_exchange.py) - index last 24h stats from TON Rocket swaps
* [MEXC indexer](etl/dags/mexc_exchange.py) - index last 24h stats from MEXC (FNZ trades)
* [Gate.io indexer](etl/dags/gate_io_exchange.py) - index last 24h stats from Gate.io (FNZ trades)
* [Data quality watchdog](etl/dags/data_quality_watchdog.py) - data quality watchdog

## Backend

To deploy:

```shell
cd backend
docker compose up -d
```
                     
Methods:
* ``GET /v1/jettons/top`` returns datamart with top Jettons
* ``GET /v1/jettons/image/{address}`` fetches jetton image and returns as image content