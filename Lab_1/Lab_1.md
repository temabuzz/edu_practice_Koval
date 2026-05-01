# Часть 1

## Шаг 1 - Создание топологии

<img width="1632" height="527" alt="изображение" src="https://github.com/user-attachments/assets/7e5fa867-7265-4a35-85e6-20a657f393fb" />

*Рис.1 Создание топологии*

## Шаг 2 - Создание сообщения на роутерах

rus-msk-r2

<img width="630" height="93" alt="изображение" src="https://github.com/user-attachments/assets/6071cc24-5f50-43e1-be75-0272b5f34292" />

*Рис.2 Создание сообщения на R2*

rus-msk-r3

<img width="625" height="86" alt="изображение" src="https://github.com/user-attachments/assets/adbb8212-1880-442e-8af4-83c49d343e1d" />

*Рис.3 Создание сообщения на R3*

rus-nsk-r1

<img width="629" height="87" alt="изображение" src="https://github.com/user-attachments/assets/9718bc6c-473f-4720-9f7c-c7c0c491d0c5" />

*Рис.4 Создание баннера на R1*


## Шаг 3 - Переименовывание устройств

Москва

| Первичная          | Измененная       |
| ------------------ | ---------------- |
| server0            | rus-msk-serv1    |
| switch0            | rus-msk-sw2      |
| router0            | rus-msk-r2       |
| router1            | rus-msk-r3       |
| multilayer switch1 | rus-msk-multisw1 |
| PC0                | rus-msk-pc6      |
| PC1                | rus-msk-pc7      |

Новосибирск

| Первичная | Измененная  |
| --------- | ----------- |
| router0   | rus-nsk-r1  |
| switch0   | rus-nsk-sw1 |
| switch1   | rus-nsk-sw2 |
| PC0       | rus-nsk-pc0 |
| PC1       | rus-nsk-pc1 |
| PC2       | rus-nsk-pc2 |
| PC3       | rus-nsk-pc3 |
| PC4       | rus-nsk-pc4 |
| PC5       | rus-nsk-pc5 |

## Шаг 4 - Раздача доменных имён
rus-msk-sw2:

<img width="276" height="20" alt="изображение" src="https://github.com/user-attachments/assets/1883a9f7-418a-4822-a18d-84355fbf5cc6" />

*Рис.5 Назначение доменного имени*

rus-msk-r2:

<img width="259" height="20" alt="изображение" src="https://github.com/user-attachments/assets/f3d8f28d-8773-49bb-ab1f-89dd5bac7bb9" />

*Рис.6 Назначение доменного имени*

rus-msk-r3:

<img width="254" height="16" alt="изображение" src="https://github.com/user-attachments/assets/89410d5e-cd8f-4cf3-adb5-633130b8627c" />

*Рис.7 Назначение доменного имени*

rus-nsk-r1:

<img width="270" height="22" alt="изображение" src="https://github.com/user-attachments/assets/9d58f363-bd7c-4be2-9677-d834e0c3112d" />

*Рис.8 Назначение доменного имени*

rus-nsk-sw0:

<img width="272" height="18" alt="изображение" src="https://github.com/user-attachments/assets/a86fe64a-b1ce-402b-affb-278c22d06b6b" />

*Рис.9 Назначеие доменного имени*

rus-nsk-sw1:

<img width="276" height="16" alt="изображение" src="https://github.com/user-attachments/assets/a93333b3-9c1b-4a13-a002-c633a0122386" />

*Рис10 Назначение доменного имени*

## Шаг 5 - Создание VLAN на коммутаторах в Нск

### rus-nsk-sw1

```bash
conf t
vlan 2
vlan 3
vlan 4
```

*Рис.7 Создание VLAN на rus-nsk-sw1*

### rus-nsk-sw2

```bash
conf t
vlan 2
vlan 3
vlan 4
```

*Рис.8 Создание VLAN на rus-nsk-sw2*

---

## Шаг 6 - Назначение VLAN на интерфейсах

### rus-nsk-sw1

```bash
interface f0/2
switchport mode access
switchport access vlan 2

interface f0/3
switchport mode access
switchport access vlan 3

interface f0/4
switchport mode access
switchport access vlan 4
```

*Рис.9 Назначение VLAN на интерфейсах rus-nsk-sw1*

### rus-nsk-sw2

```bash
interface f0/2
switchport mode access
switchport access vlan 2

interface f0/3
switchport mode access
switchport access vlan 3

interface f0/4
switchport mode access
switchport access vlan 4
```

*Рис.10 Назначение VLAN на интерфейсах rus-nsk-sw2*

---

## Шаг 7 - Создание канала между коммутаторами в Нск

### rus-nsk-sw1

```bash
interface range g0/1-2
channel-group 1 mode active

interface port-channel1
switchport mode trunk
```

*Рис.11 Создание канала на rus-nsk-sw1*

### rus-nsk-sw2

```bash
interface range g0/1-2
channel-group 1 mode passive

interface port-channel1
switchport mode trunk
```

*Рис.12 Создание канала на rus-nsk-sw2*

---

## Шаг 8 - Создание Management interface на SW1 для VLAN1

```bash
interface vlan1
ip address 1.0.0.50 255.0.0.0
no shutdown

ip default-gateway 1.0.0.1
```

*Рис.13 Management interface на SW1 для VLAN1*

---

## Шаг 9 - Management interface на SW2 для VLAN2

```bash
interface vlan2
ip address 2.0.0.50 255.0.0.0
no shutdown

ip default-gateway 2.0.0.1
```

*Рис.14 Management interface на SW2 для VLAN2*

---

## Шаг 10 - Включение SSHv2

### rus-nsk-sw1

```bash
username nsk secret cisco
ip domain-name nsk.local
crypto key generate rsa
1024
ip ssh version 2

line vty 0 15
login local
transport input ssh
```

*Рис.15 Включение SSHv2 на rus-nsk-sw1*

### rus-nsk-sw2

```bash
username nsk secret cisco
ip domain-name nsk.local
crypto key generate rsa
1024
ip ssh version 2

line vty 0 15
login local
transport input ssh
```

*Рис.16 Включение SSHv2 на rus-nsk-sw2*

---

## Шаг 11 - Настройка интерфейса f0/24

```bash
interface f0/24
switchport mode trunk
```

*Рис.17 Настройка интерфейса f0/24*

---

## Шаг 12 - Настройка баннера на SW1 и SW2

### SW1

```bash
banner motd #Это rus-nsk-sw1#
```

*Рис.18 Настройка баннера на SW1*

### SW2

```bash
banner motd #Это rus-nsk-sw2#
```

*Рис.19 Настройка баннера на SW2*

---

## Шаг 13 - Настройка f0/2-4

```bash
interface range f0/2-4
spanning-tree portfast
spanning-tree bpduguard enable
no cdp enable
switchport port-security
switchport port-security maximum 1
switchport port-security mac-address sticky
switchport port-security violation shutdown
```

*Рис.20 Настройка f0/2-4*

---

## Шаг 14 - Защита консоли

```bash
line console 0
login local
```

*Рис.21 Защита консоли*

---

## Шаг 15 - Отключение таймаута

```bash
line console 0
exec-timeout 0 0

line vty 0 15
exec-timeout 0 0
```

*Рис.22 Отключение таймаута*

---

## Шаг 16 - Отключение прерывания

```bash
line console 0
logging synchronous

line vty 0 15
logging synchronous
```

*Рис.23 Отключение прерывания*

---

## Шаг 17 - Изменение размера буфера

```bash
line console 0
history size 256
```

*Рис.24 Изменение размера буфера*

# Часть 2

## Шаг 1 - Назначение IP-адреса для F0/1 на R1

```bash
interface f0/1
ip address 40.40.40.1 255.255.255.0
no shutdown
```

*Рис.25 Назначение IP-адреса для F0/1 на R1*

---

## Шаг 2 - Настройка маршрутизации между VLAN

```bash
interface f0/0.1
encapsulation dot1Q 1 native
ip address 1.0.0.1 255.0.0.0

interface f0/0.2
encapsulation dot1Q 2
ip address 2.0.0.1 255.0.0.0

interface f0/0.3
encapsulation dot1Q 3
ip address 3.0.0.1 255.0.0.0

interface f0/0.4
encapsulation dot1Q 4
ip address 4.0.0.1 255.0.0.0
```

*Рис.26 Настройка маршрутизации между VLAN*

---

## Шаг 3 - Настройка DHCP

```bash
ip dhcp excluded-address 1.0.0.1 1.0.0.99
ip dhcp excluded-address 2.0.0.1 2.0.0.99
ip dhcp excluded-address 3.0.0.1 3.0.0.99
ip dhcp excluded-address 4.0.0.1 4.0.0.99
```

*Рис.27 Исключение адресов DHCP*

```bash
ip dhcp pool VLAN1
network 1.0.0.0 255.0.0.0
default-router 1.0.0.1
```

*Рис.28 Создание DHCP пула для VLAN1*

```bash
ip dhcp pool VLAN2
network 2.0.0.0 255.0.0.0
default-router 2.0.0.1
```

*Рис.29 Создание DHCP пула для VLAN2*

```bash
ip dhcp pool VLAN3
network 3.0.0.0 255.0.0.0
default-router 3.0.0.1
```

*Рис.30 Создание DHCP пула для VLAN3*

```bash
ip dhcp pool VLAN4
network 4.0.0.0 255.0.0.0
default-router 4.0.0.1
```

*Рис.31 Создание DHCP пула для VLAN4*

---

## Шаг 4 - Проверка настройки

```bash
ping 3.0.0.101
```

*Рис.32 Проверка ping*

# Часть 3

## Шаг 1 - Настройка имени хоста Multilayer Switch

```bash
conf t
hostname rus-msk-multisw1
```

*Рис.33 Настройка имени хоста MLS*

---

## Шаг 2 - Включение маршрутизации на MLS

```bash
ip routing
```

*Рис.34 Включение маршрутизации на MLS*

---

## Шаг 3 - Создание VLAN 100 и VLAN 200

```bash
vlan 100
name Sales_dept

vlan 200
name IT_dept
```

*Рис.35 Создание VLAN 100 и VLAN 200*

---

## Шаг 4 - Назначение VLAN на интерфейсы

```bash
interface f0/4
switchport mode access
switchport access vlan 100

interface f0/5
switchport mode access
switchport access vlan 200
```

*Рис.36 Назначение VLAN на интерфейсы*

---

## Шаг 5 - Включение маршрутизации между VLAN

```bash
interface vlan100
ip address 100.0.0.50 255.0.0.0
no shutdown

interface vlan200
ip address 200.0.0.50 255.255.255.0
no shutdown
```

*Рис.37 Включение маршрутизации между VLAN*

---

## Шаг 6 - Изменение интерфейсов f0/1-3

```bash
interface f0/1
no switchport
ip address 11.0.0.50 255.0.0.0

interface f0/2
no switchport
ip address 12.0.0.50 255.0.0.0

interface f0/3
no switchport
ip address 40.40.40.50 255.255.255.0
```

*Рис.38 Изменение интерфейсов f0/1-3*

---

## Шаг 7 - Проверка

```bash
ping 200.0.0.100
```

*Рис.39 Проверка ping*

# Часть 4

## Шаг 1 - Настройка интерфейсов R1

```bash
interface f0/0
ip address 10.0.0.2 255.0.0.0
no shutdown

interface f0/1
ip address 11.0.0.2 255.0.0.0
no shutdown
```

*Рис.40 Настройка интерфейсов R1*

---

## Шаг 2 - Настройка интерфейсов R2

```bash
interface f0/0
ip address 10.0.0.3 255.0.0.0
no shutdown

interface f0/1
ip address 12.0.0.3 255.0.0.0
no shutdown
```

*Рис.41 Настройка интерфейсов R2*

---

## Шаг 3 - Cisco High Availability

### rus-msk-r1

```bash
interface f0/0
standby 1 ip 10.0.0.1
standby 1 priority 110
standby 1 preempt
standby 1 track f0/1
```

*Рис.42 Настройка HSRP на rus-msk-r1*

### rus-msk-r2

```bash
interface f0/0
standby 1 ip 10.0.0.1
standby 1 priority 100
standby 1 preempt
```

*Рис.43 Настройка HSRP на rus-msk-r2*

# Часть 5

## Шаг 1 - Настройка EIGRP

### rus-nsk-r1

```bash
router eigrp 100
no auto-summary
network 1.0.0.0
network 2.0.0.0
network 3.0.0.0
network 4.0.0.0
network 40.40.40.0
```

*Рис.44 Настройка EIGRP на rus-nsk-r1*

### rus-msk-r1

```bash
router eigrp 100
no auto-summary
network 10.0.0.0
network 11.0.0.0
```

*Рис.45 Настройка EIGRP на rus-msk-r1*

### rus-msk-r2

```bash
router eigrp 100
no auto-summary
network 10.0.0.0
network 12.0.0.0
```

*Рис.46 Настройка EIGRP на rus-msk-r2*

### rus-msk-multisw1

```bash
router eigrp 100
no auto-summary
network 11.0.0.0
network 12.0.0.0
network 40.40.40.0
network 100.0.0.0
network 200.0.0.0
```

*Рис.47 Настройка EIGRP на rus-msk-multisw1*

---

## Шаг 2 - Проверка SSH

```bash
ssh -l nsk 1.0.0.50
ssh -l nsk 2.0.0.50
```

*Рис.48 Проверка SSH*

---

## Шаг 3 - Проверка Ping

```bash
ping 2.0.0.50
```

*Рис.49 Проверка Ping*

# Часть 6

## Шаг 1 - Ограничение SSH доступа

### rus-nsk-sw1

```bash
access-list 10 permit host 10.0.0.100
access-list 10 permit host 2.0.0.100

line vty 0 15
access-class 10 in
```

*Рис.50 Ограничение SSH доступа на rus-nsk-sw1*

### rus-nsk-sw2

```bash
access-list 10 permit host 10.0.0.100
access-list 10 permit host 2.0.0.100

line vty 0 15
access-class 10 in
```

*Рис.51 Ограничение SSH доступа на rus-nsk-sw2*

---

## Шаг 2 - Ограничение доступа к Web Server

```bash
access-list 101 permit ip host 2.0.0.100 host 10.0.0.100
access-list 101 deny ip any host 10.0.0.100
access-list 101 permit ip any any
```

*Рис.52 Ограничение доступа к Web Server*

---

## Шаг 3 - Запрет ответа на ping

### rus-msk-r1

```bash
access-list 110 deny icmp any any echo
access-list 110 permit ip any any

interface f0/0
ip access-group 110 in
```

*Рис.53 Запрет ответа на ping на rus-msk-r1*

### rus-msk-r2

```bash
access-list 110 deny icmp any any echo
access-list 110 permit ip any any

interface f0/0
ip access-group 110 in
```

*Рис.54 Запрет ответа на ping на rus-msk-r2*

# Часть 7

## Шаг 1 - Loopback на R1

```bash
interface loopback1
ip address 192.168.101.1 255.255.255.0
```

*Рис.55 Создание Loopback на R1*

---

## Шаг 2 - Loopback на R2

```bash
interface loopback3
ip address 192.168.103.3 255.255.255.0
```

*Рис.56 Создание Loopback на R2*

---

## Шаг 3 - RIPv2

### rus-nsk-r1

```bash
router rip
version 2
no auto-summary
network 10.0.0.0
network 192.168.101.0
```

*Рис.57 Настройка RIPv2 на rus-nsk-r1*

### rus-msk-r2

```bash
router rip
version 2
no auto-summary
network 10.0.0.0
network 192.168.103.0
```

*Рис.58 Настройка RIPv2 на rus-msk-r2*

---

## Шаг 4 - Ограничение RIP

На остальных устройствах RIP не включается.

---

## Шаг 5 - Настройка Tunnel

### rus-nsk-r1

```bash
interface tunnel1
ip address 200.200.200.1 255.255.255.0
tunnel source 10.0.0.2
tunnel destination 10.0.0.3
```

*Рис.59 Настройка Tunnel на rus-nsk-r1*

### rus-msk-r2

```bash
interface tunnel3
ip address 200.200.200.3 255.255.255.0
tunnel source 10.0.0.3
tunnel destination 10.0.0.2
```

*Рис.60 Настройка Tunnel на rus-msk-r2*

---

## Шаг 6 - Проверка

```bash
ping 192.168.103.3 source 192.168.101.1
```

*Рис.61 Проверка Tunnel*

# Часть 8

## Шаг 1 - NTP и Syslog

### rus-nsk-r1

```bash
ntp authentication-key 1 md5 cisco
ntp authenticate
ntp trusted-key 1
ntp server 10.0.0.100 key 1

logging 10.0.0.100
```

*Рис.62 Настройка NTP и Syslog на rus-nsk-r1*

### rus-msk-r1

```bash
ntp authentication-key 1 md5 cisco
ntp authenticate
ntp trusted-key 1
ntp server 10.0.0.100 key 1

logging 10.0.0.100
```

*Рис.63 Настройка NTP и Syslog на rus-msk-r1*

### rus-msk-r2

```bash
ntp authentication-key 1 md5 cisco
ntp authenticate
ntp trusted-key 1
ntp server 10.0.0.100 key 1

logging 10.0.0.100
```

*Рис.64 Настройка NTP и Syslog на rus-msk-r2*

---

## Шаг 2 - SNMP

### rus-msk-r1

```bash
snmp-server community cisco ro
snmp-server community cisco rw
```

*Рис.65 Настройка SNMP на rus-msk-r1*

### rus-msk-r2

```bash
snmp-server community cisco ro
snmp-server community cisco rw
```

*Рис.66 Настройка SNMP на rus-msk-r2*

---

## Шаг 3 - AAA и Telnet

### rus-msk-r2

```bash
aaa new-model
aaa authentication login default group radius local
radius-server host 10.0.0.100 key cisco

line vty 0 15
transport input telnet ssh
login authentication default
```

*Рис.67 Настройка AAA и Telnet на rus-msk-r2*

---

## Шаг 4 - Настройка FTP

```bash
ip ftp username cisco
ip ftp password cisco
```

*Рис.68 Настройка FTP*

---

## Шаг 5 - Отправка конфигурации FTP

```bash
copy running-config ftp
```

*Рис.69 Отправка конфигурации FTP*

---

## Шаг 6 - Отправка конфигурации TFTP

```bash
copy running-config tftp
```

*Рис.70 Отправка конфигурации TFTP*

---

## Шаг 7 - Проверка boot system

```bash
show run | include boot
```

*Рис.71 Проверка boot system*

---

## Шаг 8 - Проверка Telnet

### Создание пользователя

```bash
username standby secret cisco
enable secret cisco
```

*Рис.72 Создание пользователя*

### Подключение

```bash
telnet 10.0.0.3
```

*Рис.73 Подключение по Telnet*

---

## Шаг 9 - Изменение локального имени пользователя

```bash
confreg 0x2142
reload
```

*Рис.74 Сброс конфигурации*

После перезагрузки:

```bash
enable
copy startup-config running-config
conf t
no username standby
username newadmin secret cisco
config-register 0x2102
reload
```

*Рис.75 Восстановление конфигурации и создание нового пользователя*
