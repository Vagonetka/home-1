Так как отдельной виртуальной машины не было, все компоненты были развернуты на локальной машине с использованием Docker.

1 - Создан файл `docker-compose.yml` со всеми сервисами:
   - MySQL
   - WordPress (PHP-FPM)
   - Nginx
   - Node Exporter
   - MySQL Exporter
   - Nginx Exporter
   - PHP-FPM Exporter
   - Blackbox Exporter
   - Prometheus
   - Alertmanager

2 - сделал конфигурационные файлы
   - `nginx/default.conf` - настройки Nginx
   - `php/status.conf` - статус PHP-FPM
   - `mysql/init.sql` - пользователь для экспортера
   - `blackbox/config.yml` - проверка CMS
   - `GAP-1/prometheus.yml` - настройка Prometheus (сбор каждые 5 секунд)
   - `GAP-1/alerts.yml` - правила алертов
   - `GAP-1/alertmanager.yml` - настройки Alertmanager

3 - запустил систему командой `docker compose up -d`

4 - проверил работу сервисов 
