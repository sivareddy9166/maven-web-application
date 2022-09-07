# Documentaion to set locally
## Pre-Requesites
set up RabbitMQ, telegraf, influxDB, grafana locally in the system using ```docker-compose.yml```

### Configuration changes in telegraf.conf 

1. Use ```telegraf.conf``` to configure telegraf, influxDb and RabbitMQ.
2. Change the hostname to store_id(which is not used yet).

### Changes in app.py in BR 

Comment the adminpanallogger process in ```app.py```.

### Changes in config.py in BR 

1. Change the ```vms_ip``` in calss ```GeneralConfig``` which is locally taken by BrowserRefreshment and TelegrafLogger.
2. Replace status_check IP with Local IP in class ```RabbitMQConsumerConfig```.
3. Decrease the period count in class ```TelegrafLoggerConfig``` for testing BR locally (initially it has 5 mins time period which is too high and take more time for testing).

## Procedure

#### Create a miniconda env with name ```browser-refreshment```
install the ```requrements.txt```
#### Start all the services using docker-compose
```docker-compose up -d```

#### Start BR by running ```python3 app.py```


