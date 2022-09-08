# Documentaion to set locally
## Pre-Requesites
set up RabbitMQ, telegraf, influxDB, grafana locally in the system using ```docker-compose.test.yml``` file in test_services dir.

### Configuration changes in telegraf.conf 

1. Use ```telegraf.conf``` file in test_services dir to configure telegraf, influxDb and RabbitMQ.
2. Change the hostname to store_id(store_id which is not used yet in any store).

### Configuring grafana
Connect grafana using ```http://127.1.0.0:3000``` and configure influxDB 

### Changes in config.py in BR 

* Use ```debug : true``` in class ```GeneralConfig``` while testing locally 

## Procedure

#### Create a miniconda env with name ```browser-refreshment```
install the ```requrements.txt```

#### Start all the services using docker-compose
```docker-compose up -d```

#### Start BR by running ```python3 app.py```
