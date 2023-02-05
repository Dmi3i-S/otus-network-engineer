# lab7. VxLAN 3.
### Цель: 
Настроить отказоустойчивое подключение клиентов с использованием VPC.
- Подключите клиентов 2-я линками к различным Leaf.
- Настроите агрегированный канал со стороны клиента.
- Настроите VPC для работы в Overlay сети.
### Порядок работы:
- За основу использована схема сети из lab6. VxLAN 2.
- Конфигурации Spine1, Spine2, Leaf3 остались без изменений.
- Leaf1 и Leaf2 подключены с помощью VPC. 
- Leaf2 переведен в bgp AS 65521.
- В качестве клиента Host1 использован коммутатор, подключен через агрегированный канал LACP к Leaf1 и Leaf2.
- Добавлен ip address 10.111.1.1/32 secondary в Loopback1 на Leaf1 и Leaf2.
- В interface nve1 добавлена команда advertise virtual-rmac на Leaf1 и Leaf2.
- В router bgp 65521, в address-family l2vpn evpn добавлена команда advertise-pip на Leaf1 и Leaf2.
### Результат:
- Схема сети с VPC.
![Схема сети с VPC](Схема%20VXLAN%20с%20VPC.jpg)
- Распределение адресного пространства.
![Адресное пространство](Распределение%20адресного%20пространства.md)
- Файлы с конфигурациями Nexus9K и клиентами:
- Конфигурация
![Spine1](Spine1_config.txt)
- Конфигурация
![Spine2](Spine2_config.txt)
- Конфигурация VPC
![для Leaf1 и Leaf2](vpc_config.txt)
- Конфигурация
![Leaf1](Leaf1_config.txt)
- Конфигурация
![Leaf2](Leaf2_config.txt)
- Конфигурация
![Leaf3](Leaf3_config.txt)
- Конфигурация клиента
![Host1](Host1_config.txt)
- Конфигурации клиентов
![Hosts2-3](Hosts.txt)
- Результаты диагностики VPC
![Вывод команд](Diagnostic%20vpc.txt)
