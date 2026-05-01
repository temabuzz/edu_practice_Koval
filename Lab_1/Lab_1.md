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

## Шаг 5 - Создание VLAN 2, 3, 4 на коммутаторах в Нск

rus-nsk-sw1:

<img width="152" height="84" alt="изображение" src="https://github.com/user-attachments/assets/e4aa15bf-0bf8-4893-9741-3153f485f2a5" />

*Рис.7 Создание VLAN на rus-nsk-sw1*

rus-nsk-sw2

<img width="152" height="87" alt="изображение" src="https://github.com/user-attachments/assets/67cf9584-a719-4080-8bf7-adbef43941e9" />

*Рис.8 Создание VLAN на rus-nsk-sw2*

## Шаг 6 - Назначение VLAN на интерфейсах

rus-nsk-sw0:

<img width="308" height="145" alt="изображение" src="https://github.com/user-attachments/assets/b229400d-e3db-4704-81bb-0208e81c8ecd" />

*Рис.9 Назначение VLAN на интерфейсах rus-nsk-sw0*

rus-nsk-sw1

<img width="301" height="153" alt="изображение" src="https://github.com/user-attachments/assets/57e17846-bf50-4e74-8f98-016c6aa4f39b" />

*Рис.10 Назначение VLAN на интерфейсах rus-nsk-sw1*

---

## Шаг 7 - Создание канала между коммутаторами в Новосибисрке

### rus-nsk-sw1

<img width="367" height="57" alt="изображение" src="https://github.com/user-attachments/assets/5b987f1a-184f-4fe6-8c83-857ee404b531" />

*Рис.11 Создание канала на rus-nsk-sw1*

### rus-nsk-sw2

<img width="355" height="56" alt="изображение" src="https://github.com/user-attachments/assets/a7ecfa7a-ccb3-42a7-a135-61db00501fec" />

*Рис.12 Создание канала на rus-nsk-sw2*


## Шаг 8 - Создание Management interface на SW1 для VLAN1

<img width="328" height="91" alt="изображение" src="https://github.com/user-attachments/assets/fb68f051-4ab3-408b-b3eb-ec22aa040b3e" />

*Рис.13 Management interface на SW1 для VLAN1*

## Шаг 9 - Management interface на SW2 для VLAN2

<img width="337" height="58" alt="изображение" src="https://github.com/user-attachments/assets/66933a5b-5c52-45b1-b4b9-45f9a6035023" />

*Рис.14 Management interface на SW2 для VLAN2*

## Шаг 10 - Включение SSHv2

### rus-nsk-sw1

<img width="517" height="212" alt="изображение" src="https://github.com/user-attachments/assets/3f237abd-0cac-4d68-a09c-4e49b749d91c" />

*Рис.15 Включение SSHv2 на rus-nsk-sw1*

### rus-nsk-sw2

<img width="517" height="212" alt="изображение" src="https://github.com/user-attachments/assets/3f147247-d510-4c62-895e-f4507696aba8" />

*Рис.16 Включение SSHv2 на rus-nsk-sw2*

## Шаг 11 - Настройка интерфейса f0/24

<img width="269" height="30" alt="изображение" src="https://github.com/user-attachments/assets/b380a19f-0460-4749-9185-91929ab234ef" />

*Рис.17 Настройка интерфейса f0/24*

## Шаг 12 - Настройка баннера на SW1 и SW2

### SW1

<img width="300" height="17" alt="изображение" src="https://github.com/user-attachments/assets/84df2877-2594-49fc-aa9e-fb6b536930e0" />

*Рис.18 Настройка баннера на SW1*

### SW2

<img width="294" height="14" alt="изображение" src="https://github.com/user-attachments/assets/82804424-c77b-4c6d-b454-e043c73588ff" />

*Рис.19 Настройка баннера на SW2*

## Шаг 13 - Настройка f0/2-4 на SW0 и SW1

rus-nsk-sw0:

<img width="515" height="408" alt="изображение" src="https://github.com/user-attachments/assets/5a8b0c15-0191-40c9-a170-b49a2f08a909" />

*Рис.20 Настройка f0/2-4*

rus-nsk-sw1:

<img width="526" height="406" alt="изображение" src="https://github.com/user-attachments/assets/dde8f0c2-9cdb-40a3-98a5-79b66d84f4d2" />

## Шаг 14 - Защита консоли
rus-nsk-sw0:

<img width="209" height="30" alt="изображение" src="https://github.com/user-attachments/assets/502ebe72-5ded-43aa-9ea8-7ef159994474" />

*Рис.21 Защита консоли*
rus-msk-sw1:

<img width="203" height="30" alt="изображение" src="https://github.com/user-attachments/assets/dbd22a2f-d6da-4b15-b608-5fed2c8c6501" />

*Рис.21 Защита консоли*

## Шаг 15 - Отключение таймаута
rus-nsk-sw0:

<img width="252" height="72" alt="изображение" src="https://github.com/user-attachments/assets/1f7e5088-68b8-4386-8149-3c227df0ccad" />

*Рис.22 Отключение таймаута*

rus-nsk-sw1:

<img width="251" height="70" alt="изображение" src="https://github.com/user-attachments/assets/56fd021c-eb95-405e-bb1a-c1b075e53560" />

*Рис.22 Отключение таймаута*

## Шаг 16 - Отключение прерывания

rus-nsk-sw0:

<img width="266" height="70" alt="изображение" src="https://github.com/user-attachments/assets/9782d87d-8c01-41af-b11b-76478c46eac5" />


rus-nsk-sw1:

<img width="274" height="73" alt="изображение" src="https://github.com/user-attachments/assets/ca7e84b9-a08f-466f-b428-e64d77df2989" />


## Шаг 17 - Изменение размера буфера

rus-nsk-sw0:

<img width="220" height="15" alt="изображение" src="https://github.com/user-attachments/assets/9516ad28-aace-40c1-8879-eba7828aa199" />

rus-nsk-sw1:

<img width="207" height="14" alt="изображение" src="https://github.com/user-attachments/assets/09cc1639-976c-42b5-bd68-64ff9a02413d" />

# Часть 2

## Шаг 1 - Назначение IP-адреса для F0/1 на R1
rus-nsk-r1:

<img width="365" height="45" alt="изображение" src="https://github.com/user-attachments/assets/58105f2b-9344-4634-bd17-929b7dd5a668" />

*Рис.25 Назначение IP-адреса для F0/1 на R1*

## Шаг 2 - Настройка маршрутизации между VLAN на R1

<img width="337" height="210" alt="изображение" src="https://github.com/user-attachments/assets/f1c1a7bd-b9c0-4348-9f82-21ed3d1e469c" />

*Рис.26 Настройка маршрутизации между VLAN*

## Шаг 3 - Настройка R1 в качетсве DHCP-сервера

<img width="374" height="57" alt="изображение" src="https://github.com/user-attachments/assets/009180cd-9186-4560-be82-66597254d015" />

*Рис.27 Исключение адресов DHCP*

<img width="299" height="167" alt="изображение" src="https://github.com/user-attachments/assets/27c21421-af8a-4b78-9e7a-cc4d2dbed09a" />

*Рис.28 Создание DHCP пула для VLAN*

## Шаг 4 - Проверка настройки

<img width="403" height="185" alt="изображение" src="https://github.com/user-attachments/assets/4ede3b35-6b4e-434e-ac11-3334b8cb3553" />

*Рис.32 Проверка ping*

# Часть 3

## Шаг 1 - Настройка имени хоста Multilayer Switch

<img width="434" height="56" alt="изображение" src="https://github.com/user-attachments/assets/24b9166d-0893-4aa5-9fc7-13e1dd97fa64" />

*Рис.33 Настройка имени хоста MLS*

## Шаг 2 - Включение маршрутизации на MLS

<img width="175" height="17" alt="изображение" src="https://github.com/user-attachments/assets/af216dc9-7646-487b-9b83-39971702994d" />

*Рис.34 Включение маршрутизации на MLS*

## Шаг 3 - Создание VLAN 100 и VLAN 200 и присваивание им имён

<img width="237" height="53" alt="изображение" src="https://github.com/user-attachments/assets/66c76397-ab2f-486f-b48e-e68345ad3bcc" />

*Рис.35 Создание VLAN 100 и VLAN 200*

## Шаг 4 - Назначение VLAN на интерфейсы f0/4-5

<img width="319" height="86" alt="изображение" src="https://github.com/user-attachments/assets/06beb7e3-af9a-4d40-b7f6-44c77cbc1f0a" />

*Рис.36 Назначение VLAN на интерфейсы*

## Шаг 5 - Включение маршрутизации между VLAN

<img width="360" height="83" alt="изображение" src="https://github.com/user-attachments/assets/43af5639-260b-45fc-abfb-41a76ab5971f" />

*Рис.37 Включение маршрутизации между VLAN*

## Шаг 6 - Изменение интерфейсов f0/1-3

<img width="367" height="127" alt="изображение" src="https://github.com/user-attachments/assets/969dd367-3684-434d-8f71-3da361c8f342" />

*Рис.38 Изменение интерфейсов f0/1-3*

## Шаг 7 - Проверка

<img width="395" height="190" alt="изображение" src="https://github.com/user-attachments/assets/e261ca93-cfaa-417c-a517-b9a0620ea1e1" />

*Рис.39 Проверка ping*

# Часть 4

## Шаг 1 - Настройка интерфейсов R2

<img width="317" height="100" alt="изображение" src="https://github.com/user-attachments/assets/e14834b2-bf9d-47d9-9a27-1da0f1ac47b6" />

*Рис.40 Настройка интерфейсов R2*


## Шаг 2 - Настройка интерфейсов R3

<img width="307" height="98" alt="изображение" src="https://github.com/user-attachments/assets/9e500a2f-1cc6-4429-8a20-f81e0adfd5f4" />

*Рис.41 Настройка интерфейсов R3*

## Шаг 3 - Настройка Cisco High Availability

### rus-msk-r2

<img width="262" height="68" alt="изображение" src="https://github.com/user-attachments/assets/82cd2a4a-c20d-429e-80df-f83bea2cc8f3" />

*Рис.42 Настройка Cisco High Availability на rus-msk-r2*

### rus-msk-r3

<img width="260" height="43" alt="изображение" src="https://github.com/user-attachments/assets/d0e72c25-8610-4bfc-b4f1-6c5ea7c1cb4a" />

*Рис.43 Настройка Cisco High Availability на rus-msk-r3*

# Часть 5

## Шаг 1 - Настройка EIGRP

### rus-nsk-r1

<img width="262" height="95" alt="изображение" src="https://github.com/user-attachments/assets/5bdae0c6-700d-4a2d-8979-124277c4d8da" />

*Рис.44 Настройка EIGRP на rus-nsk-r1*

### rus-msk-r2

<img width="252" height="57" alt="изображение" src="https://github.com/user-attachments/assets/4760c8fc-c51d-4eca-9f9a-433277c06ce3" />

*Рис.45 Настройка EIGRP на rus-msk-r2*

### rus-msk-r3

<img width="254" height="58" alt="изображение" src="https://github.com/user-attachments/assets/0b12baa2-0d0a-4396-9a41-b7c49c7e102b" />

*Рис.46 Настройка EIGRP на rus-msk-r3*

### rus-msk-multisw1

<img width="270" height="99" alt="изображение" src="https://github.com/user-attachments/assets/5174390e-fed3-447f-9cd3-e0c3f11df7c3" />

*Рис.47 Настройка EIGRP на rus-msk-multisw1*

---

## Шаг 2 - Проверка SSH
Подключение SSH с сервера на rus-nsk-sw0:

<img width="176" height="103" alt="изображение" src="https://github.com/user-attachments/assets/56af4d37-62c2-48b4-8ada-845bc3ca5604" />

*Рис.48 Проверка SSH на sw0*

Подключение SSH с сервера на rus-nsk-sw1:

<img width="177" height="110" alt="изображение" src="https://github.com/user-attachments/assets/6ddf1d0e-affa-4d9b-817e-48f3cfa37769" />

*Рис.48 Проверка SSH на sw1*


---

## Шаг 3 - Проверка Ping c сервера

<img width="403" height="188" alt="изображение" src="https://github.com/user-attachments/assets/b9639abc-95da-46da-8363-f89de682f9e4" />

*Рис.49 Проверка Ping*

# Часть 6

## Шаг 1 - Ограничение SSH доступа к sw0 и sw1

### rus-nsk-sw0

<img width="349" height="56" alt="изображение" src="https://github.com/user-attachments/assets/bb418633-5e82-4691-a474-5bc4a69c9fe8" />

*Рис.50 Ограничение SSH доступа на rus-nsk-sw0*

### rus-nsk-sw1

<img width="351" height="58" alt="изображение" src="https://github.com/user-attachments/assets/dbd3786e-d9dd-476a-be5d-a5d2d926995f" />

*Рис.51 Ограничение SSH доступа на rus-nsk-sw1*

---

## Шаг 2 - Ограничение доступа к Web Server 
rus-nsk-r1:

<img width="464" height="45" alt="изображение" src="https://github.com/user-attachments/assets/30412fd0-a80f-4142-882a-87bee6518be5" />

*Рис.52 Ограничение доступа к Web Server*

---

## Шаг 3 - Запрет ответа на ping

### rus-msk-r2

<img width="359" height="56" alt="изображение" src="https://github.com/user-attachments/assets/96df3fff-178d-40b3-8a01-f4f29e547ffd" />

*Рис.53 Запрет ответа на ping на rus-msk-r2*

### rus-msk-r3

<img width="357" height="58" alt="изображение" src="https://github.com/user-attachments/assets/268adabb-3b16-4431-b879-43ee0dba2bec" />

*Рис.54 Запрет ответа на ping на rus-msk-r3*

# Часть 7

## Шаг 1 - Loopback на R1
rus-nsk-r1:

<img width="383" height="42" alt="изображение" src="https://github.com/user-attachments/assets/8a987dd4-42b1-4483-8b04-31cedcf4db37" />

*Рис.55 Создание Loopback на R1*

---

## Шаг 2 - Loopback на R3
rus-msk-r3:

<img width="371" height="42" alt="изображение" src="https://github.com/user-attachments/assets/674eb672-20b6-4321-81b4-97dfeef91cda" />

*Рис.56 Создание Loopback на R3*

---

## Шаг 3 - Настройка анонсирования Loopback-интерфейса через RIPv2
### rus-nsk-r1

<img width="284" height="73" alt="изображение" src="https://github.com/user-attachments/assets/d14ca264-dc91-4eaa-bac5-2444f2674b41" />

*Рис.57 Настройка RIPv2 на rus-nsk-r1*

### rus-msk-r3

<img width="287" height="73" alt="изображение" src="https://github.com/user-attachments/assets/1f9f0e78-3074-4160-a2a3-059a9505d5f3" />

*Рис.58 Настройка RIPv2 на rus-msk-r3*

---

## Шаг 4 - Ограничение RIP
rus-msk-r2:

<img width="179" height="18" alt="изображение" src="https://github.com/user-attachments/assets/2133ec61-b55d-4c23-91e1-29ba687e7ba8" />

rus-msk-multisw1:

<img width="194" height="17" alt="изображение" src="https://github.com/user-attachments/assets/b8eed2a9-efbf-4ea9-9728-1d24fd28eb8c" />


## Шаг 5 - Настройка Tunnel

### rus-nsk-r1

<img width="408" height="112" alt="изображение" src="https://github.com/user-attachments/assets/8ca4edd6-4c98-4662-8ea3-9ca18a8fa960" />

*Рис.59 Настройка Tunnel на rus-nsk-r1*

### rus-msk-r3


*Рис.60 Настройка Tunnel на rus-msk-r3*

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
