# Prometheus + Grafana + AlertManager project (EN)
Docker-compose grafana+prometheus+am project

This project involves launching a combination of Prometheus + Grafana + AlertManager services in docker-compose.
To access the grafana dashboard, you need to enter
 #### login: admin
 #### password: admin
as stated in the grafana - environment section

## Prometheus
This service is running on open standard port 9090, you need to go to the service page
http://localhost:9090
 - ```./prometeus``` - The docker-compose file contains a folder containing the settings of objects for monitoring
 - ```./prom-data``` - a folder that will be automatically created when the service starts, it will contain the prometheus database

## AlertManager
This service is launched on port 9093, to manage alerts you need to go to
http://localhost:9093
 - ```./alertmanager``` - this folder contains configurations of monitored alerts and their thresholds

## Grafana
This service is running on port 3000, to monitor the metrics you need to go to  
http://localhost:3000
- ```./grafana/dashboards``` - the folder in which configurations for provisioning dashboards are configured through the config ```./grafana/dashboards/dashboard.yml```, all created JSON dashboards must be copied to this folder and restarted grafana for rereading configs
- ```./grafana/datasources``` - the folder in which configurations for provisioning data sources are configured through the config ```./grafana/datasources.datasource.yml```, all created JSON data sources must be copied to this folder and restarted grafana for rereading configs

### Grafana Environment
In this section, docker-compose has defined the authorization parameters for accessing the grafana service.  
- admin/admin  

## Service management
- ```docker-compose up -d``` - compile and start the service
- ```docker-compose down``` - stop the service
- ```docker-compose restart``` - restart the service

_________________________________________________  
# Prometheus + Grafana + AlertManager project (RU)
Docker-compose grafana+prometheus+am project

Данный проект подразумевает запуск в docker-compose сочетание сервисов Prometheus + Grafana + AlertManager.
Для доступа к дашборду grafana, нужно ввести  
 #### login: admin  
 #### password: admin  
как это указано в разделе grafana - environment

## Prometheus
Данный сервис запущен на открытом стандартном порту 9090, на страницу сервиса нужно перейти   
http://localhost:9090  
 - ```./prometeus``` - В docker-compose файле вынесена папка в которой находятся настройки объектов для мониторинга
 - ```./prom-data``` - папка, которая автоматически создастся при запуске сервиса, в ней будет находится БД prometheus

## AlertManager
Данный сервис запущен на порту 9093, для управления алертами нужно перейти  
http://localhost:9093  
 - ```./alertmanager``` - в данной папке находятся конфигурации наблюдаемых алертов и их пороги

## Grafana
Данный сервис запущен на порту 3000, для наблюдения за метриками нужно перейти  
http://localhost:3000  
- ```./grafana/dashboards``` - папка в которой настроены конфигурации о провижининге дашбордов через конфиг ```./grafana/dashboards/dashboard.yml```, все создаваемые JSON дашборды необходимо копировать в данную папку и перезапускать grafana для перечитывания конфигов
- ```./grafana/datasources``` - папка в которой настроены конфигурации о провижининге датасоурсов через конфиг ```./grafana/datasources.datasource.yml```, все создаваемые JSON датасоурсы необходимо копировать в данную папку и перезапускать grafana для перечитывания конфигов

### Grafana Environment
В данном разделе docker-compose обозначил параметры авторизации для доступа к сервису графаны.  
- admin/admin


## Управление сервисом
- ```docker-compose up -d``` - собрать и запустить сервис  
- ```docker-compose down``` - остановить сервис  
- ```docker-compose restart``` - перезапустить сервис  
