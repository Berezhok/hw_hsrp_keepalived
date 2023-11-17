# Задание по теме "ОТКАЗОУСТОЙЧИВОСТЬ семейство протоколов FHRP" Бережок Антон
## Задание 1
### Дана схема для Cisco Packet Tracer, рассматриваемая в лекции.
### На данной схеме уже настроено отслеживание интерфейсов маршрутизаторов Gi0/1 (для нулевой группы)
### необходимо аналогично настроить отслеживание состояния интерфейсов Gi0/0 (для первой группы).
### Для проверки корректности настройки, разорвите один из кабелей между одним из маршрутизаторов и Switch0 и запустите ping между PC0 и Server0.
### На проверку отправьте получившуюся схему в формате pkt и скриншот, где виден процесс настройки маршрутизатора.
### Был отключен порт верхнего роутера, у которого приоритет выше изначально
### ![](https://github.com/Berezhok/hw_hsrp_keepalived/blob/main/img/cisco.png)
### Пинг и соединения все равно проходили, настройки и скриншоты представлены
### ![](https://github.com/Berezhok/hw_hsrp_keepalived/blob/main/img/ping.png)
### ![](https://github.com/Berezhok/hw_hsrp_keepalived/blob/main/img/router1_show_stand.png)
### ![](https://github.com/Berezhok/hw_hsrp_keepalived/blob/main/img/router2_show_stand.png)
## Задание 2
### Запустили две виртуальные машины Linux, установили и настроили Keepalived.
### Настрили веб-сервер Nginx на двух виртуальных машинах
### Написали Bash-скрипт, который будет проверять доступность порта данного веб-сервера и существование файла index.html в root-директории данного веб-сервера.
### ![](https://github.com/Berezhok/hw_hsrp_keepalived/blob/main/img/script.png)
### Конфигурационные файлы MASTER и BACKUP 
### ![](https://github.com/Berezhok/hw_hsrp_keepalived/blob/main/img/conf_MASTER.png)
### ![](https://github.com/Berezhok/hw_hsrp_keepalived/blob/main/img/conf_BACKUP.png)
### При нормальной работе у МАСТЕРА отображается плавающий ip
### ![](https://github.com/Berezhok/hw_hsrp_keepalived/blob/main/img/master_ip_float+.png)
### При остановке сервиса Nginx VirtualIp исчезает из списка MASTERA
### ![](https://github.com/Berezhok/hw_hsrp_keepalived/blob/main/img/master_ip_float_no.png)