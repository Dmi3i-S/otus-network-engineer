# lab5. VxLAN 1.
### Цель:
Настроить Overlay на основе VxLAN EVPN для L2 связанности между клиентами.
- Настроить BGP peering между Leaf и Spine в AF l2vpn evpn.
- Настроить связанность между клиентами в первой зоне.
### Результат:
- Схема сети с VxLAN EVPN L2.
![Схема сети с VxLAN EVPN L2](Схема%20VXLAN1.jpg)
- Распределение адресного пространства. Для связности хостам назначены IP-адреса из одной сети 10.4.1.0/24. 
![Адресное пространство](Распределение%20адресного%20пространства.md)
- Файлы с конфигурациями Nexus9K и клиентами:
- Конфигурация
![Spine1](Spine1%20config.txt)
- Конфигурация
![Spine2](Spine2%20config.txt)
- Конфигурация
![Leaf1](Leaf1%20config.txt)
- Конфигурация
![Leaf2](Leaf2%20config.txt)
- Конфигурация
![Leaf3](Leaf3%20config.txt)
- Конфигурации клиентов
![Hosts1-4](Hosts%20config.txt)
- Вывод команды show bgp l2vpn evpn
![show bgp l2vpn evpn](show%20bgp%20l2vpn%20evpn.txt)
- Вывод команды show nve peers
![show nve peers](show%20nve%20peers.txt)
