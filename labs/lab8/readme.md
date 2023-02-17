# lab8. VxLAN 4.
### Цель: 
Реализовать передачу суммарных префиксов через EVPN route-type 5
- Анонсируете суммарные префиксы клиентов в Overlay сеть.
- Настроите маршрутизацию между клиентами через суммарный префикс.
### Порядок работы:
- За основу взята схема из ДЗ VXLAN1. Клиенты 1-4 подключены к Leaf1 и Leaf2. Клиенты 1 и 3 - vlan 100, vrf AA. Клиенты 2 и 4 - vlan 200, vrf BB.
- Leaf3 получил роль BorderLeaf без подключенных клиентов.
- К BorderLeaf подключен FireWall, обеспечивает доступность между клиентами в vrf AA и vrf BB.
### Результат:
- Схема сети.
![Схема сети](Схема_VXLAN4.jpg)
- Распределение адресного пространства.
![Адресное пространство](Распределение%20адресного%20пространства.md)
- Файлы с конфигурациями Nexus9K и клиентами:
- Конфигурация
![Spine1](Spine1_config.txt)
- Конфигурация
![Spine2](Spine2_config.txt)
- Конфигурация
![Leaf1](Leaf1_config.txt)
- Конфигурация
![Leaf2](Leaf2_config.txt)
- Конфигурация
![BorderLeaf](BorderLeaf_config.txt)
- Конфигурация
![FireWall](FireWall_config.txt)
- Конфигурации клиентов
![Hosts1-4](Hosts1-4_config.txt)
- Результаты диагностики BGP neighbors
![Вывод команд](Diagnostic_BGP_neighbors.txt)
- Результаты диагностики BGP Route 
![Вывод команд](Diagnostic_BGP_route.txt)
- Результаты диагностики BorderLeaf
![Вывод команд](Diagnostic_BorderLeaf.txt)
- Результаты диагностики c клиентов Host1 и 2
![Вывод команд](Diagnostic%20from%20Host1-2.txt)
- Результаты диагностики c клиентов Host3 и 4
![Вывод команд](Diagnostic%20from%20Host3-4.txt)
