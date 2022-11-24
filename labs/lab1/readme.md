# lab1. Проектирование адресного пространства.
### Цель:
Собрать схему CLOS.
Распределить адресное пространство.
### Результат:
- Схема сети
![Схема сети](Схема%20Net%20Clos.jpg)
- Адресное пространство

| Узел/Хост | Тип интерфейса | Адрес | Description |
| ----------- | ---------- | -------- | ---------- |
| Spine1 | Loopback 0 | 10.0.1.1/32 |
|      | p2p | 10.2.1.0/31 | p2p links between Spine1 and Leaf1 |
|      | p2p | 10.2.1.2/31 | p2p links between Spine1 and Leaf2 |
|      | p2p | 10.2.1.4/31 | p2p links between Spine1 and Leaf3 |
| Spine2 | Loopback 0 | 10.0.2.1/32 |
|      | p2p | 10.2.2.0/31 | p2p links between Spine2 and Leaf1 |
|      | p2p | 10.2.2.2/31 | p2p links between Spine2 and Leaf2 |
|      | p2p | 10.2.2.4/31 | p2p links between Spine2 and Leaf3 |
| Leaf1 | Loopback 0 | 10.1.1.1/32 | 
| Leaf1 | Ethernet 1/1 | 10.4.1.1/30 | p2p link Leaf1 |
| Host1 | Ethernet 0 | 10.4.1.2/30 | p2p link Host1 |
| Leaf2 | Loopback 0 | 10.1.2.1/32 |
| Leaf2 | Ethernet 1/1 | 10.4.2.1/30 | p2p link Leaf2 |
| Host2 | Ethernet 0 | 10.4.2.2/30 | p2p link Host2 |
| Leaf3 | Loopback 0 | 10.1.3.1/32 |
| Leaf3 | Ethernet 1/1 | 10.4.3.1/30 | p2p link Leaf3 (to Host3) |
| Host3 | Ethernet 0 | 10.4.3.2/30 | p2p link Host3 |
| Leaf3 | Ethernet 1/2 | 10.4.3.5/30 | p2p link Leaf3 (to Host4) | 
| Host4 | Ethernet 0 | 10.4.3.6/30 | p2p link Host4 |
