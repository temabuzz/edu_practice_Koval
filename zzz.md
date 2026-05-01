
# Полное выполнение задания Configure LAN Part1

Источник задания: PDF-файл пользователя fileciteturn0file0

Сеть большая, люди любят страдать через Packet Tracer, поэтому делаем всё по шагам.

---

# ЧАСТЬ 1

## Шаг 1. Построй топологию

Собери сеть по схеме из PDF.

---

## Шаг 2. Настрой MOTD на всех роутерах

На каждом роутере:

```bash
conf t
banner motd #Работу выполнил(а) студент группы 321#
end
wr
```

---

## Шаг 3. Переименование устройств

Пример:

```bash
R1 -> rus-msk-r1
R2 -> rus-msk-r2
R3 -> rus-msk-r3
SW0 -> rus-nsk-sw0
SW1 -> rus-nsk-sw1
MLS -> rus-msk-mls
```

Команда:

```bash
conf t
hostname rus-msk-r1
end
wr
```

---

## Шаг 4. Настрой доменные имена

На всех устройствах:

```bash
conf t
ip domain-name local.lab
end
wr
```

---

## Шаг 5. Создай VLAN на SW0 и SW1

На SW0 и SW1:

```bash
conf t
vlan 2
vlan 3
vlan 4
end
wr
```

---

## Шаг 6. Назначь порты VLAN

На SW0 и SW1:

```bash
conf t
interface f0/2
switchport mode access
switchport access vlan 2

interface f0/3
switchport mode access
switchport access vlan 3

interface f0/4
switchport mode access
switchport access vlan 4
end
wr
```

---

## Шаг 7. EtherChannel между SW0 и SW1

На SW0:

```bash
conf t
interface range g0/1 - 2
channel-group 1 mode active
exit

interface port-channel 1
switchport mode trunk
end
wr
```

На SW1:

```bash
conf t
interface range g0/1 - 2
channel-group 1 mode passive
exit

interface port-channel 1
switchport mode trunk
end
wr
```

---

## Шаг 8. Management IP на SW0

```bash
conf t
interface vlan 1
ip address 1.0.0.50 255.0.0.0
no shutdown
exit

ip default-gateway 1.0.0.1
end
wr
```

---

## Шаг 9. Management IP на SW1

```bash
conf t
interface vlan 2
ip address 2.0.0.50 255.0.0.0
no shutdown
exit

ip default-gateway 2.0.0.1
end
wr
```

---

## Шаг 10. SSHv2

На SW0 и SW1:

```bash
conf t
username nsk privilege 15 secret cisco
ip domain-name local.lab
crypto key generate rsa
1024
ip ssh version 2

line vty 0 15
login local
transport input ssh
end
wr
```

---

## Шаг 11. Сделай f0/24 trunk

```bash
conf t
interface f0/24
switchport mode trunk
end
wr
```

---

## Шаг 12. MOTD на коммутаторах

```bash
conf t
banner motd #Это rus-nsk-sw0#
end
wr
```

---

## Шаг 13. Настройка портов доступа

```bash
conf t
interface range f0/2 - 4
spanning-tree portfast
spanning-tree bpduguard enable
switchport port-security
switchport port-security maximum 1
switchport port-security mac-address sticky
switchport port-security violation shutdown
no cdp enable
end
wr
```

---

## Шаг 14. Защита консоли

```bash
conf t
line console 0
login local
end
wr
```

---

## Шаг 15. Убрать timeout

```bash
conf t
line console 0
exec-timeout 0 0

line vty 0 15
exec-timeout 0 0
end
wr
```

---

## Шаг 16. Отключить прерывание логами

```bash
conf t
line console 0
logging synchronous
end
wr
```

---

## Шаг 17. История команд

```bash
terminal history size 256
```

---

# ЧАСТЬ 2

## Шаг 1. Настрой f0/1 на R1

```bash
conf t
interface f0/1
ip address 40.40.40.1 255.255.255.0
no shutdown
end
wr
```

---

## Шаг 2. Router-on-a-stick

```bash
conf t
interface f0/0
no shutdown

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
end
wr
```

---

## Шаг 3. DHCP

```bash
conf t

ip dhcp excluded-address 1.0.0.1 1.0.0.99
ip dhcp excluded-address 1.0.0.201 1.0.0.254

ip dhcp excluded-address 2.0.0.1 2.0.0.99
ip dhcp excluded-address 2.0.0.201 2.0.0.254

ip dhcp excluded-address 3.0.0.1 3.0.0.99
ip dhcp excluded-address 3.0.0.201 3.0.0.254

ip dhcp excluded-address 4.0.0.1 4.0.0.99
ip dhcp excluded-address 4.0.0.201 4.0.0.254

ip dhcp pool VLAN1
network 1.0.0.0 255.0.0.0
default-router 1.0.0.1

ip dhcp pool VLAN2
network 2.0.0.0 255.0.0.0
default-router 2.0.0.1

ip dhcp pool VLAN3
network 3.0.0.0 255.0.0.0
default-router 3.0.0.1

ip dhcp pool VLAN4
network 4.0.0.0 255.0.0.0
default-router 4.0.0.1
end
wr
```

---

# ЧАСТЬ 3

## MLS

```bash
conf t
hostname MLS
ip routing

vlan 100
name Sales_dept

vlan 200
name IT_dept

interface f0/4
switchport mode access
switchport access vlan 100

interface f0/5
switchport mode access
switchport access vlan 200

interface vlan 100
ip address 100.0.0.50 255.0.0.0
no shutdown

interface vlan 200
ip address 200.0.0.50 255.255.255.0
no shutdown

interface f0/1
no switchport
ip address 11.0.0.50 255.0.0.0
no shutdown

interface f0/2
no switchport
ip address 12.0.0.50 255.0.0.0
no shutdown

interface f0/3
no switchport
ip address 40.40.40.50 255.255.255.0
no shutdown
end
wr
```

---

# ЧАСТЬ 4

## R2

```bash
conf t
interface f0/0
ip address 10.0.0.2 255.0.0.0
no shutdown

interface f0/1
ip address 11.0.0.2 255.0.0.0
no shutdown
end
wr
```

## R3

```bash
conf t
interface f0/0
ip address 10.0.0.3 255.0.0.0
no shutdown

interface f0/1
ip address 12.0.0.3 255.0.0.0
no shutdown
end
wr
```

---

## HSRP

На R2:

```bash
conf t
interface f0/0
standby 1 ip 10.0.0.1
standby 1 priority 110
standby 1 preempt
standby 1 track f0/1
end
wr
```

На R3:

```bash
conf t
interface f0/0
standby 1 ip 10.0.0.1
standby 1 priority 100
standby 1 preempt
end
wr
```

---

# ЧАСТЬ 5

## EIGRP

На R1, R2, R3, MLS:

```bash
conf t
router eigrp 100
no auto-summary
network 0.0.0.0
end
wr
```

---

# ЧАСТЬ 6

## SSH только для нужных устройств

На SW1:

```bash
conf t
access-list 10 permit host 10.0.0.100
access-list 10 permit host 2.0.0.100

line vty 0 15
access-class 10 in
end
wr
```

---

## Доступ к web серверу только с 2.0.0.100

На маршрутизаторе:

```bash
conf t
access-list 101 permit ip host 2.0.0.100 host 10.0.0.100
access-list 101 deny ip any host 10.0.0.100
access-list 101 permit ip any any

interface f0/0
ip access-group 101 in
end
wr
```

---

## R2 и R3 не отвечают на ping

На R2 и R3:

```bash
conf t
access-list 110 deny icmp any any echo
access-list 110 permit ip any any

interface f0/0
ip access-group 110 in

interface f0/1
ip access-group 110 in
end
wr
```

---

# ЧАСТЬ 7

## Loopback

На R1:

```bash
conf t
interface loopback1
ip address 192.168.101.1 255.255.255.0
end
wr
```

На R3:

```bash
conf t
interface loopback3
ip address 192.168.103.3 255.255.255.0
end
wr
```

---

## RIP v2

На R1:

```bash
conf t
router rip
version 2
no auto-summary
network 192.168.101.0
network 40.0.0.0
end
wr
```

На R3:

```bash
conf t
router rip
version 2
no auto-summary
network 192.168.103.0
network 12.0.0.0
end
wr
```

---

## Tunnel

На R1:

```bash
conf t
interface tunnel1
ip address 200.200.200.1 255.255.255.0
tunnel source f0/1
tunnel destination 12.0.0.3
no shutdown
end
wr
```

На R3:

```bash
conf t
interface tunnel3
ip address 200.200.200.3 255.255.255.0
tunnel source f0/1
tunnel destination 40.40.40.1
no shutdown
end
wr
```

---

## Добавить RIP в туннель

На R1 и R3:

```bash
conf t
router rip
network 200.200.200.0
end
wr
```

---

# ЧАСТЬ 8

## NTP + Syslog

На R1/R2/R3/MLS:

```bash
conf t
ntp authentication-key 1 md5 cisco
ntp authenticate
ntp trusted-key 1
ntp server 10.0.0.100 key 1

logging 10.0.0.100
end
wr
```

---

## SNMP на R2 и R3

```bash
conf t
snmp-server community cisco RO
snmp-server community cisco RW
end
wr
```

---

## AAA + Telnet на R3

```bash
conf t
aaa new-model
radius-server host 10.0.0.100 key cisco

username standby secret cisco

aaa authentication login default group radius local

line vty 0 4
transport input telnet ssh
login authentication default
end
wr
```

---

## FTP на R2

```bash
conf t
ip ftp username cisco
ip ftp password cisco
end
wr
```

---

## Копия конфига FTP

```bash
copy running-config ftp:
```

FTP Server:

```bash
10.0.0.100
```

---

## Копия конфига TFTP

На R3:

```bash
copy running-config tftp:
```

TFTP:

```bash
10.0.0.100
```

---

## Проверка boot system

```bash
show running-config | include boot
```

Если есть:

```bash
conf t
no boot system
end
wr
```

---

## Проверка telnet

С R2:

```bash
telnet 10.0.0.3
```

Логин:

```bash
standby
```

Пароль:

```bash
cisco
```

---

## Смена пользователя через recovery

На R3:

```bash
conf t
no username standby
username admin secret cisco
end
wr
```

---

Готово. Люди называют это «лабораторная». На деле это марафон по конфигам Cisco.
