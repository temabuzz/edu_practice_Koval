# Часть 1

## Шаг 1 - Создание топологии

<img width="1632" height="527" alt="изображение" src="https://github.com/user-attachments/assets/7e5fa867-7265-4a35-85e6-20a657f393fb" />

*Рис. 1 Создание топологии*

## Шаг 2 - Создание сообщения на роутерах

rus-msk-r2:

<img width="630" height="93" alt="изображение" src="https://github.com/user-attachments/assets/6071cc24-5f50-43e1-be75-0272b5f34292" />

*Рис. 2 Создание сообщения на R2*

rus-msk-r3:

<img width="625" height="86" alt="изображение" src="https://github.com/user-attachments/assets/adbb8212-1880-442e-8af4-83c49d343e1d" />

*Рис. 3 Создание сообщения на R3*

rus-nsk-r1:

<img width="629" height="87" alt="изображение" src="https://github.com/user-attachments/assets/9718bc6c-473f-4720-9f7c-c7c0c491d0c5" />

*Рис. 4 Создание баннера на R1*


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
| switch0   | rus-nsk-sw0 |
| switch1   | rus-nsk-sw1 |
| PC0       | rus-nsk-pc0 |
| PC1       | rus-nsk-pc1 |
| PC2       | rus-nsk-pc2 |
| PC3       | rus-nsk-pc3 |
| PC4       | rus-nsk-pc4 |
| PC5       | rus-nsk-pc5 |

## Шаг 4 - Раздача доменных имён

rus-msk-sw2:

<img width="276" height="20" alt="изображение" src="https://github.com/user-attachments/assets/1883a9f7-418a-4822-a18d-84355fbf5cc6" />

*Рис. 5 Назначение доменного имени*

rus-msk-r2:

<img width="259" height="20" alt="изображение" src="https://github.com/user-attachments/assets/f3d8f28d-8773-49bb-ab1f-89dd5bac7bb9" />

*Рис. 6 Назначение доменного имени*

rus-msk-r3:

<img width="254" height="16" alt="изображение" src="https://github.com/user-attachments/assets/89410d5e-cd8f-4cf3-adb5-633130b8627c" />

*Рис. 7 Назначение доменного имени*

rus-nsk-r1:

<img width="270" height="22" alt="изображение" src="https://github.com/user-attachments/assets/9d58f363-bd7c-4be2-9677-d834e0c3112d" />

*Рис. 8 Назначение доменного имени*

rus-nsk-sw0:

<img width="272" height="18" alt="изображение" src="https://github.com/user-attachments/assets/a86fe64a-b1ce-402b-affb-278c22d06b6b" />

*Рис. 9 Назначение доменного имени*

rus-nsk-sw1:

<img width="276" height="16" alt="изображение" src="https://github.com/user-attachments/assets/a93333b3-9c1b-4a13-a002-c633a0122386" />

*Рис. 10 Назначение доменного имени*

## Шаг 5 - Создание VLAN 2, 3, 4 на коммутаторах в Нск

rus-nsk-sw0:

<img width="152" height="84" alt="изображение" src="https://github.com/user-attachments/assets/e4aa15bf-0bf8-4893-9741-3153f485f2a5" />

*Рис. 11 Создание VLAN на rus-nsk-sw0*

rus-nsk-sw1:

<img width="152" height="87" alt="изображение" src="https://github.com/user-attachments/assets/67cf9584-a719-4080-8bf7-adbef43941e9" />

*Рис. 12 Создание VLAN на rus-nsk-sw1*

## Шаг 6 - Назначение VLAN на интерфейсах

rus-nsk-sw0:

<img width="308" height="145" alt="изображение" src="https://github.com/user-attachments/assets/b229400d-e3db-4704-81bb-0208e81c8ecd" />

*Рис. 13 Назначение VLAN на интерфейсах rus-nsk-sw0*

rus-nsk-sw1:

<img width="301" height="153" alt="изображение" src="https://github.com/user-attachments/assets/57e17846-bf50-4e74-8f98-016c6aa4f39b" />

*Рис. 14 Назначение VLAN на интерфейсах rus-nsk-sw1*

## Шаг 7 - Создание канала между коммутаторами в Новосибисрке

rus-nsk-sw0:

<img width="367" height="57" alt="изображение" src="https://github.com/user-attachments/assets/5b987f1a-184f-4fe6-8c83-857ee404b531" />

*Рис. 15 Создание канала на rus-nsk-sw0*

rus-nsk-sw1:

<img width="355" height="56" alt="изображение" src="https://github.com/user-attachments/assets/a7ecfa7a-ccb3-42a7-a135-61db00501fec" />

*Рис. 16 Создание канала на rus-nsk-sw1*

## Шаг 8 - Создание Management interface на SW0 для VLAN1

<img width="328" height="91" alt="изображение" src="https://github.com/user-attachments/assets/fb68f051-4ab3-408b-b3eb-ec22aa040b3e" />

*Рис. 17 Management interface на SW0 для VLAN1*

## Шаг 9 - Management interface на SW1 для VLAN2

<img width="337" height="58" alt="изображение" src="https://github.com/user-attachments/assets/66933a5b-5c52-45b1-b4b9-45f9a6035023" />

*Рис. 18 Management interface на SW1 для VLAN2*

## Шаг 10 - Включение SSHv2

rus-nsk-sw0:

<img width="517" height="212" alt="изображение" src="https://github.com/user-attachments/assets/3f237abd-0cac-4d68-a09c-4e49b749d91c" />

*Рис. 19 Включение SSHv2 на rus-nsk-sw0*

rus-nsk-sw1:

<img width="517" height="212" alt="изображение" src="https://github.com/user-attachments/assets/3f147247-d510-4c62-895e-f4507696aba8" />

*Рис. 20 Включение SSHv2 на rus-nsk-sw1*

## Шаг 11 - Настройка интерфейса f0/24

<img width="269" height="30" alt="изображение" src="https://github.com/user-attachments/assets/b380a19f-0460-4749-9185-91929ab234ef" />

*Рис. 21 Настройка интерфейса f0/24*

## Шаг 12 - Настройка баннера на SW1 и SW2

SW0:

<img width="300" height="17" alt="изображение" src="https://github.com/user-attachments/assets/84df2877-2594-49fc-aa9e-fb6b536930e0" />

*Рис. 22 Настройка баннера на SW0*

SW1:

<img width="294" height="14" alt="изображение" src="https://github.com/user-attachments/assets/82804424-c77b-4c6d-b454-e043c73588ff" />

*Рис. 23 Настройка баннера на SW1*

## Шаг 13 - Настройка f0/2-4 на SW0 и SW1

rus-nsk-sw0:

<img width="515" height="408" alt="изображение" src="https://github.com/user-attachments/assets/5a8b0c15-0191-40c9-a170-b49a2f08a909" />

*Рис. 24 Настройка f0/2-4*

rus-nsk-sw1:

<img width="526" height="406" alt="изображение" src="https://github.com/user-attachments/assets/dde8f0c2-9cdb-40a3-98a5-79b66d84f4d2" />

*Рис. 25 Настройка f0/2-4*

## Шаг 14 - Защита консоли

rus-nsk-sw0:

<img width="209" height="30" alt="изображение" src="https://github.com/user-attachments/assets/502ebe72-5ded-43aa-9ea8-7ef159994474" />

*Рис. 26 Защита консоли*

rus-msk-sw1:

<img width="203" height="30" alt="изображение" src="https://github.com/user-attachments/assets/dbd22a2f-d6da-4b15-b608-5fed2c8c6501" />

*Рис. 27 Защита консоли*

## Шаг 15 - Отключение таймаута

rus-nsk-sw0:

<img width="252" height="72" alt="изображение" src="https://github.com/user-attachments/assets/1f7e5088-68b8-4386-8149-3c227df0ccad" />

*Рис. 28 Отключение таймаута*

rus-nsk-sw1:

<img width="251" height="70" alt="изображение" src="https://github.com/user-attachments/assets/56fd021c-eb95-405e-bb1a-c1b075e53560" />

*Рис. 29 Отключение таймаута*

## Шаг 16 - Отключение прерывания

rus-nsk-sw0:

<img width="266" height="70" alt="изображение" src="https://github.com/user-attachments/assets/9782d87d-8c01-41af-b11b-76478c46eac5" />

*Рис. 30 Отключение прерывания*

rus-nsk-sw1:

<img width="274" height="73" alt="изображение" src="https://github.com/user-attachments/assets/ca7e84b9-a08f-466f-b428-e64d77df2989" />

*Рис. 31 Отключение прерывания*

## Шаг 17 - Изменение размера буфера

rus-nsk-sw0:

<img width="220" height="15" alt="изображение" src="https://github.com/user-attachments/assets/9516ad28-aace-40c1-8879-eba7828aa199" />

*Рис. 32 Изменение размера буфера*

rus-nsk-sw1:

<img width="207" height="14" alt="изображение" src="https://github.com/user-attachments/assets/09cc1639-976c-42b5-bd68-64ff9a02413d" />

*Рис. 33 Изменение размера буфера*

# Часть 2

## Шаг 1 - Назначение IP-адреса для F0/1 на R1

rus-nsk-r1:

<img width="365" height="45" alt="изображение" src="https://github.com/user-attachments/assets/58105f2b-9344-4634-bd17-929b7dd5a668" />

*Рис. 34 Назначение IP-адреса для F0/1 на R1*

## Шаг 2 - Настройка маршрутизации между VLAN на R1

<img width="337" height="210" alt="изображение" src="https://github.com/user-attachments/assets/f1c1a7bd-b9c0-4348-9f82-21ed3d1e469c" />

*Рис. 35 Настройка маршрутизации между VLAN*

## Шаг 3 - Настройка R1 в качетсве DHCP-сервера

<img width="374" height="57" alt="изображение" src="https://github.com/user-attachments/assets/009180cd-9186-4560-be82-66597254d015" />

*Рис. 36 Исключение адресов DHCP*

<img width="299" height="167" alt="изображение" src="https://github.com/user-attachments/assets/27c21421-af8a-4b78-9e7a-cc4d2dbed09a" />

*Рис. 37 Создание DHCP пула для VLAN*

## Шаг 4 - Проверка настройки

<img width="403" height="185" alt="изображение" src="https://github.com/user-attachments/assets/4ede3b35-6b4e-434e-ac11-3334b8cb3553" />

*Рис. 38 Проверка ping*

# Часть 3

## Шаг 1 - Настройка имени хоста Multilayer Switch

<img width="434" height="56" alt="изображение" src="https://github.com/user-attachments/assets/24b9166d-0893-4aa5-9fc7-13e1dd97fa64" />

*Рис. 39 Настройка имени хоста MLS*

## Шаг 2 - Включение маршрутизации на MLS

<img width="175" height="17" alt="изображение" src="https://github.com/user-attachments/assets/af216dc9-7646-487b-9b83-39971702994d" />

*Рис. 40 Включение маршрутизации на MLS*

## Шаг 3 - Создание VLAN 100 и VLAN 200 и присваивание им имён

<img width="237" height="53" alt="изображение" src="https://github.com/user-attachments/assets/66c76397-ab2f-486f-b48e-e68345ad3bcc" />

*Рис. 41 Создание VLAN 100 и VLAN 200*

## Шаг 4 - Назначение VLAN на интерфейсы f0/4-5

<img width="319" height="86" alt="изображение" src="https://github.com/user-attachments/assets/06beb7e3-af9a-4d40-b7f6-44c77cbc1f0a" />

*Рис. 42 Назначение VLAN на интерфейсы*

## Шаг 5 - Включение маршрутизации между VLAN

<img width="360" height="83" alt="изображение" src="https://github.com/user-attachments/assets/43af5639-260b-45fc-abfb-41a76ab5971f" />

*Рис. 43 Включение маршрутизации между VLAN*

## Шаг 6 - Изменение интерфейсов f0/1-3

<img width="367" height="127" alt="изображение" src="https://github.com/user-attachments/assets/969dd367-3684-434d-8f71-3da361c8f342" />

*Рис. 44 Изменение интерфейсов f0/1-3*

## Шаг 7 - Проверка

<img width="395" height="190" alt="изображение" src="https://github.com/user-attachments/assets/e261ca93-cfaa-417c-a517-b9a0620ea1e1" />

*Рис. 45 Проверка ping*

# Часть 4

## Шаг 1 - Настройка интерфейсов R2

<img width="317" height="100" alt="изображение" src="https://github.com/user-attachments/assets/e14834b2-bf9d-47d9-9a27-1da0f1ac47b6" />

*Рис. 46 Настройка интерфейсов R2*

## Шаг 2 - Настройка интерфейсов R3

<img width="307" height="98" alt="изображение" src="https://github.com/user-attachments/assets/9e500a2f-1cc6-4429-8a20-f81e0adfd5f4" />

*Рис. 47 Настройка интерфейсов R3*

## Шаг 3 - Настройка Cisco High Availability

rus-msk-r2:

<img width="262" height="68" alt="изображение" src="https://github.com/user-attachments/assets/82cd2a4a-c20d-429e-80df-f83bea2cc8f3" />

*Рис. 48 Настройка Cisco High Availability на rus-msk-r2*

rus-msk-r3:

<img width="260" height="43" alt="изображение" src="https://github.com/user-attachments/assets/d0e72c25-8610-4bfc-b4f1-6c5ea7c1cb4a" />

*Рис. 49 Настройка Cisco High Availability на rus-msk-r3*

# Часть 5

## Шаг 1 - Настройка EIGRP

rus-nsk-r1:

<img width="262" height="95" alt="изображение" src="https://github.com/user-attachments/assets/5bdae0c6-700d-4a2d-8979-124277c4d8da" />

*Рис. 50 Настройка EIGRP на rus-nsk-r1*

rus-msk-r2:

<img width="252" height="57" alt="изображение" src="https://github.com/user-attachments/assets/4760c8fc-c51d-4eca-9f9a-433277c06ce3" />

*Рис. 51 Настройка EIGRP на rus-msk-r2*

rus-msk-r3:

<img width="254" height="58" alt="изображение" src="https://github.com/user-attachments/assets/0b12baa2-0d0a-4396-9a41-b7c49c7e102b" />

*Рис. 52 Настройка EIGRP на rus-msk-r3*

rus-msk-multisw1:

<img width="270" height="99" alt="изображение" src="https://github.com/user-attachments/assets/5174390e-fed3-447f-9cd3-e0c3f11df7c3" />

*Рис. 53 Настройка EIGRP на rus-msk-multisw1*

## Шаг 2 - Проверка SSH

Подключение SSH с сервера на rus-nsk-sw0:

<img width="176" height="103" alt="изображение" src="https://github.com/user-attachments/assets/56af4d37-62c2-48b4-8ada-845bc3ca5604" />

*Рис. 54 Проверка SSH на sw0*

Подключение SSH с сервера на rus-nsk-sw1:

<img width="177" height="110" alt="изображение" src="https://github.com/user-attachments/assets/6ddf1d0e-affa-4d9b-817e-48f3cfa37769" />

*Рис. 55 Проверка SSH на sw1*

## Шаг 3 - Проверка Ping c сервера

<img width="403" height="188" alt="изображение" src="https://github.com/user-attachments/assets/b9639abc-95da-46da-8363-f89de682f9e4" />

*Рис. 56 Проверка Ping*

# Часть 6

## Шаг 1 - Ограничение SSH доступа к sw0 и sw1

rus-nsk-sw0:

<img width="349" height="56" alt="изображение" src="https://github.com/user-attachments/assets/bb418633-5e82-4691-a474-5bc4a69c9fe8" />

*Рис. 57 Ограничение SSH доступа на rus-nsk-sw0*

rus-nsk-sw1:

<img width="351" height="58" alt="изображение" src="https://github.com/user-attachments/assets/dbd3786e-d9dd-476a-be5d-a5d2d926995f" />

*Рис. 58 Ограничение SSH доступа на rus-nsk-sw1*

## Шаг 2 - Ограничение доступа к Web Server

rus-nsk-r1:

<img width="464" height="45" alt="изображение" src="https://github.com/user-attachments/assets/30412fd0-a80f-4142-882a-87bee6518be5" />

*Рис. 59 Ограничение доступа к Web Server*

## Шаг 3 - Запрет ответа на ping

rus-msk-r2:

<img width="359" height="56" alt="изображение" src="https://github.com/user-attachments/assets/96df3fff-178d-40b3-8a01-f4f29e547ffd" />

*Рис. 60 Запрет ответа на ping на rus-msk-r2*

rus-msk-r3:

<img width="357" height="58" alt="изображение" src="https://github.com/user-attachments/assets/268adabb-3b16-4431-b879-43ee0dba2bec" />

*Рис. 61 Запрет ответа на ping на rus-msk-r3*

# Часть 7

## Шаг 1 - Loopback на R1

rus-nsk-r1:

<img width="383" height="42" alt="изображение" src="https://github.com/user-attachments/assets/8a987dd4-42b1-4483-8b04-31cedcf4db37" />

*Рис. 62 Создание Loopback на R1*

## Шаг 2 - Loopback на R3

rus-msk-r3:

<img width="371" height="42" alt="изображение" src="https://github.com/user-attachments/assets/674eb672-20b6-4321-81b4-97dfeef91cda" />

*Рис. 63 Создание Loopback на R3*

## Шаг 3 - Настройка анонсирования Loopback-интерфейса через RIPv2

rus-nsk-r1:

<img width="284" height="73" alt="изображение" src="https://github.com/user-attachments/assets/d14ca264-dc91-4eaa-bac5-2444f2674b41" />

*Рис. 64 Настройка RIPv2 на rus-nsk-r1*

rus-msk-r3:

<img width="287" height="73" alt="изображение" src="https://github.com/user-attachments/assets/1f9f0e78-3074-4160-a2a3-059a9505d5f3" />

*Рис. 65 Настройка RIPv2 на rus-msk-r3*

## Шаг 4 - Ограничение RIP

rus-msk-r2:

<img width="179" height="18" alt="изображение" src="https://github.com/user-attachments/assets/2133ec61-b55d-4c23-91e1-29ba687e7ba8" />

*Рис. 66 Ограничение RIP на rus-msk-r2*

rus-msk-multisw1:

<img width="194" height="17" alt="изображение" src="https://github.com/user-attachments/assets/b8eed2a9-efbf-4ea9-9728-1d24fd28eb8c" />

*Рис. 67 Ограничение RIP на rus-msk-multisw1*

## Шаг 5 - Настройка Tunnel

rus-nsk-r1:

<img width="408" height="112" alt="изображение" src="https://github.com/user-attachments/assets/8ca4edd6-4c98-4662-8ea3-9ca18a8fa960" />

*Рис. 68 Настройка Tunnel на rus-nsk-r1*

rus-msk-r3:

<img width="386" height="58" alt="изображение" src="https://github.com/user-attachments/assets/24ca012c-72f1-4a83-8182-bc57f72313c2" />

*Рис. 69 Настройка Tunnel на rus-msk-r3*

## Шаг 6 - Проверка loopback-интерфейса

<img width="550" height="326" alt="изображение" src="https://github.com/user-attachments/assets/f033f5b5-62e5-48f5-8678-8e333de386b2" />

*Рис. 70 Проверка loopback-интерфейса*

# Часть 8

## Шаг 1 - NTP и Syslog

rus-nsk-r1:

<img width="319" height="70" alt="изображение" src="https://github.com/user-attachments/assets/f108099b-5931-497f-931c-74852bd49b3a" />

*Рис. 71 Настройка NTP и Syslog на rus-nsk-r1*

rus-msk-r2:

<img width="326" height="71" alt="изображение" src="https://github.com/user-attachments/assets/e1d7ace9-522a-415e-bd48-684600dd1aea" />

*Рис. 72 Настройка NTP и Syslog на rus-msk-r2*

rus-msk-r3:

<img width="320" height="68" alt="изображение" src="https://github.com/user-attachments/assets/51291cca-47a1-42db-a4e7-bdf8c204e2e8" />

*Рис. 73 Настройка NTP и Syslog на rus-msk-r3*

## Шаг 2 - Настройка SNMP на R2 и R3

rus-msk-r2:

<img width="297" height="32" alt="изображение" src="https://github.com/user-attachments/assets/36e1a1bf-6c5b-4f8e-83b5-3c0c85740796" />

*Рис. 74 Настройка SNMP на rus-msk-r2*

rus-msk-r3:

<img width="304" height="28" alt="изображение" src="https://github.com/user-attachments/assets/62c69c2c-d7ae-432c-8392-803dbefca57d" />

*Рис. 75 Настройка SNMP на rus-msk-r3*

## Шаг 3 - Настройка AAA и Telnet на r3

rus-msk-r3:

<img width="468" height="83" alt="изображение" src="https://github.com/user-attachments/assets/b2b47547-72c4-414d-b241-729f2a22be00" />

*Рис. 76 Настройка AAA и Telnet на rus-msk-r3*

## Шаг 4 - Настройка FTP

rus-msk-r2:

<img width="233" height="27" alt="изображение" src="https://github.com/user-attachments/assets/c2e8eed5-5ba7-4b96-a0a1-a883a0e3e697" />

*Рис. 77 Настройка FTP*

## Шаг 5 - Отправка конфигурации FTP

<img width="356" height="114" alt="изображение" src="https://github.com/user-attachments/assets/0978ee29-18d3-4e9e-a2d6-e46aa493cab3" />

*Рис. 78 Отправка конфигурации FTP*

## Шаг 6 - Отправка конфигурации TFTP

<img width="330" height="114" alt="изображение" src="https://github.com/user-attachments/assets/5fe00289-ad11-41fe-997c-3787a2f26822" />

*Рис. 79 Отправка конфигурации TFTP*

## Шаг 7 - Проверка boot system

<img width="191" height="30" alt="изображение" src="https://github.com/user-attachments/assets/d09acb78-aa6d-4c35-8b85-151dab321319" />

*Рис. 80 Проверка boot system*

Команда ничего не выдаёт, значит команд boot system нет.

## Шаг 8 - Проверка Telnet

Создание пользователя

rus-msk-r3:

<img width="286" height="29" alt="изображение" src="https://github.com/user-attachments/assets/5ef6d3d1-9e44-4303-9f73-a13b13a8a600" />

*Рис. 81 Создание пользователя*

rus-msk-r2:

<img width="612" height="152" alt="изображение" src="https://github.com/user-attachments/assets/3c857a40-700f-41fb-85f4-90a5bc8715c2" />

*Рис. 82 Подключение по Telnet*

## Шаг 9 - Изменение локального имени пользователя на R3

Вводим команду для игнорирования конфигурации при загрузке.

<img width="193" height="17" alt="изображение" src="https://github.com/user-attachments/assets/a67fac0a-3181-42e8-ad2f-f56726396edb" />

*Рис. 83 Сброс конфигурации*

После перезагрузки:

<img width="643" height="338" alt="изображение" src="https://github.com/user-attachments/assets/3f2bb438-c87e-41d7-bf8f-8f5ebbe2a4cd" />

*Рис. 84 Восстановление конфигурации и создание нового пользователя*

# Полная конфигурация
rus-nsk-r1:
```
!
version 15.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname R1
!
!
!
!
ip dhcp excluded-address 1.0.0.1 1.0.0.99
ip dhcp excluded-address 1.0.0.201 1.0.0.254
ip dhcp excluded-address 2.0.0.1 2.0.0.99
ip dhcp excluded-address 2.0.0.201 2.0.0.254
ip dhcp excluded-address 3.0.0.1 3.0.0.99
ip dhcp excluded-address 3.0.0.201 3.0.0.254
ip dhcp excluded-address 4.0.0.1 4.0.0.99
ip dhcp excluded-address 4.0.0.201 4.0.0.254
!
ip dhcp pool VLAN1
 network 1.0.0.0 255.0.0.0
 default-router 1.0.0.1
 dns-server 8.8.8.8
ip dhcp pool VLAN2
 network 2.0.0.0 255.0.0.0
 default-router 2.0.0.1
 dns-server 8.8.8.8
ip dhcp pool VLAN3
 network 3.0.0.0 255.0.0.0
 default-router 3.0.0.1
 dns-server 8.8.8.8
ip dhcp pool VLAN4
 network 4.0.0.0 255.0.0.0
 default-router 4.0.0.1
 dns-server 8.8.8.8
!
!
!
no ip cef
no ipv6 cef
!
!
!
!
license udi pid CISCO2811/K9 sn FTX1017ZTUG-
!
!
!
!
!
!
!
!
!
ip domain-name nsk.local
!
!
spanning-tree mode pvst
!
!
!
!
!
!
interface Loopback0
 ip address 192.168.101.1 255.255.255.0
!
interface Tunnel0
 ip address 200.200.200.1 255.255.255.0
 mtu 1476
 tunnel source FastEthernet0/1
 tunnel destination 10.0.0.3
!
!
interface FastEthernet0/0
 no ip address
 duplex auto
 speed auto
!
interface FastEthernet0/0.1
 encapsulation dot1Q 1 native
 ip address 1.0.0.1 255.0.0.0
!
interface FastEthernet0/0.2
 encapsulation dot1Q 2
 ip address 2.0.0.1 255.0.0.0
 ip access-group 110 in
!
interface FastEthernet0/0.3
 encapsulation dot1Q 3
 ip address 3.0.0.1 255.0.0.0
!
interface FastEthernet0/0.4
 encapsulation dot1Q 4
 ip address 4.0.0.1 255.0.0.0
!
interface FastEthernet0/1
 ip address 40.40.40.1 255.255.255.0
 duplex auto
 speed auto
!
interface Vlan1
 no ip address
 shutdown
!
router eigrp 100
 network 1.0.0.0
 network 2.0.0.0
 network 3.0.0.0
 network 4.0.0.0
 network 40.40.40.0 0.0.0.255
!
router rip
 version 2
 network 192.168.101.0
 network 200.200.200.0
 no auto-summary
!
ip classless
!
ip flow-export version 9
!
!
access-list 110 permit tcp host 2.0.0.100 host 10.0.0.100 eq www
access-list 110 deny tcp 2.0.0.0 0.255.255.255 host 10.0.0.100 eq www
access-list 110 permit ip any any
!
banner motd #Rabotu vypolnil Koval' Artem student gruppy 9SA-321, v zhurnale pod nomerom 12!#
!
!
!
!
logging 10.0.0.100
line con 0
!
line aux 0
!
line vty 0 4
 login
!
!
ntp authentication-key 1 md5 0822455D0A16 7
ntp authenticate
ntp trusted-key 1
ntp server 10.0.0.100 key 1
!
end
```
rus-nsk-sw0:
```
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname SW0
!
!
!
ip ssh version 2
ip domain-name nsk.local
!
username nsk secret 5 $1$mERr$hx5rVt7rPNoS4wqbXKX7m0
!
!
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface Port-channel1
 switchport mode trunk
!
interface FastEthernet0/1
!
interface FastEthernet0/2
 switchport access vlan 2
 switchport mode access
 switchport port-security mac-address sticky 
 no cdp enable
 spanning-tree portfast
 spanning-tree bpduguard enable
!
interface FastEthernet0/3
 switchport access vlan 3
 switchport mode access
 switchport port-security mac-address sticky 
 no cdp enable
 spanning-tree portfast
 spanning-tree bpduguard enable
!
interface FastEthernet0/4
 switchport access vlan 4
 switchport mode access
 switchport port-security mac-address sticky 
 no cdp enable
 spanning-tree portfast
 spanning-tree bpduguard enable
!
interface FastEthernet0/5
!
interface FastEthernet0/6
!
interface FastEthernet0/7
!
interface FastEthernet0/8
!
interface FastEthernet0/9
!
interface FastEthernet0/10
!
interface FastEthernet0/11
!
interface FastEthernet0/12
!
interface FastEthernet0/13
!
interface FastEthernet0/14
!
interface FastEthernet0/15
!
interface FastEthernet0/16
!
interface FastEthernet0/17
!
interface FastEthernet0/18
!
interface FastEthernet0/19
!
interface FastEthernet0/20
!
interface FastEthernet0/21
!
interface FastEthernet0/22
!
interface FastEthernet0/23
!
interface FastEthernet0/24
 switchport mode trunk
!
interface GigabitEthernet0/1
 switchport mode trunk
 channel-group 1 mode active
!
interface GigabitEthernet0/2
 switchport mode trunk
 channel-group 1 mode active
!
interface Vlan1
 ip address 1.0.0.50 255.0.0.0
!
ip default-gateway 1.0.0.1
!
banner motd #Eto rus-nsk-sw0#
!
!
!
access-list 10 permit host 10.0.0.100
access-list 10 permit host 2.0.0.100
line con 0
 logging synchronous
 login local
 history size 256
 exec-timeout 0 0
!
line vty 0 4
 access-class 10 in
 exec-timeout 0 0
 login local
 transport input ssh
line vty 5 15
 access-class 10 in
 exec-timeout 0 0
 login local
 transport input ssh
!
!
!
!
end
```
rus-nsk-sw1:
```
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname SW1
!
!
!
ip ssh version 2
ip domain-name nsk.local
!
username nsk secret 5 $1$mERr$hx5rVt7rPNoS4wqbXKX7m0
!
!
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface Port-channel1
 switchport mode trunk
!
interface FastEthernet0/1
 shutdown
!
interface FastEthernet0/2
 switchport access vlan 2
 switchport mode access
 switchport port-security mac-address sticky 
 no cdp enable
 spanning-tree portfast
 spanning-tree bpduguard enable
!
interface FastEthernet0/3
 switchport access vlan 3
 switchport mode access
 switchport port-security mac-address sticky 
 no cdp enable
 spanning-tree portfast
 spanning-tree bpduguard enable
!
interface FastEthernet0/4
 switchport access vlan 4
 switchport mode access
 switchport port-security mac-address sticky 
 no cdp enable
 spanning-tree portfast
 spanning-tree bpduguard enable
!
interface FastEthernet0/5
!
interface FastEthernet0/6
!
interface FastEthernet0/7
!
interface FastEthernet0/8
!
interface FastEthernet0/9
!
interface FastEthernet0/10
!
interface FastEthernet0/11
!
interface FastEthernet0/12
!
interface FastEthernet0/13
!
interface FastEthernet0/14
!
interface FastEthernet0/15
!
interface FastEthernet0/16
!
interface FastEthernet0/17
!
interface FastEthernet0/18
!
interface FastEthernet0/19
!
interface FastEthernet0/20
!
interface FastEthernet0/21
!
interface FastEthernet0/22
!
interface FastEthernet0/23
!
interface FastEthernet0/24
!
interface GigabitEthernet0/1
 switchport mode trunk
 channel-group 1 mode passive
!
interface GigabitEthernet0/2
 switchport mode trunk
 channel-group 1 mode passive
!
interface Vlan1
 no ip address
 shutdown
!
interface Vlan2
 ip address 2.0.0.50 255.0.0.0
!
ip default-gateway 2.0.0.1
!
banner motd #Eto rus-nsk-sw1#
!
!
!
access-list 10 permit host 10.0.0.100
access-list 10 permit host 2.0.0.100
line con 0
 logging synchronous
 login local
 history size 256
 exec-timeout 0 0
!
line vty 0 4
 access-class 10 in
 exec-timeout 0 0
 login local
 transport input ssh
line vty 5 15
 access-class 10 in
 exec-timeout 0 0
 login local
 transport input ssh
!
!
!
!
end
```
rus-msk-sw2:
```
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname SW2
!
!
!
ip domain-name msk.local
!
!
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface FastEthernet0/1
!
interface FastEthernet0/2
!
interface FastEthernet0/3
!
interface FastEthernet0/4
!
interface FastEthernet0/5
!
interface FastEthernet0/6
!
interface FastEthernet0/7
!
interface FastEthernet0/8
!
interface FastEthernet0/9
!
interface FastEthernet0/10
!
interface FastEthernet0/11
!
interface FastEthernet0/12
!
interface FastEthernet0/13
!
interface FastEthernet0/14
!
interface FastEthernet0/15
!
interface FastEthernet0/16
!
interface FastEthernet0/17
!
interface FastEthernet0/18
!
interface FastEthernet0/19
!
interface FastEthernet0/20
!
interface FastEthernet0/21
!
interface FastEthernet0/22
!
interface FastEthernet0/23
!
interface FastEthernet0/24
!
interface GigabitEthernet0/1
!
interface GigabitEthernet0/2
!
interface Vlan1
 no ip address
 shutdown
!
!
!
!
line con 0
!
line vty 0 4
 login
line vty 5 15
 login
!
!
!
!
end
```
rus-msk-r2:
```
!
version 15.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname R2
!
!
!
!
!
!
!
!
no ip cef
no ipv6 cef
!
!
!
!
license udi pid CISCO2811/K9 sn FTX10173D5Q-
!
!
!
!
!
!
!
!
!
ip ftp username cisco
ip ftp password cisco
ip domain-name msk.local
!
!
spanning-tree mode pvst
!
!
!
!
!
!
interface FastEthernet0/0
 ip address 10.0.0.2 255.0.0.0
 ip access-group 120 in
 duplex auto
 speed auto
 standby 1 ip 10.0.0.1
 standby 1 preempt
 standby 1 track FastEthernet0/1
!
interface FastEthernet0/1
 ip address 11.0.0.2 255.0.0.0
 ip access-group 120 in
 duplex auto
 speed auto
!
interface Vlan1
 no ip address
 shutdown
!
router eigrp 100
 network 10.0.0.0
 network 11.0.0.0
!
ip classless
!
ip flow-export version 9
!
!
access-list 120 permit icmp any any echo-reply
access-list 120 deny icmp any any echo
access-list 120 permit ip any any
!
banner motd #Rabotu vypolnil Koval' Artem student gruppy 9SA-321, v zhurnale pod nomerom 12!#
!
!
!
snmp-server community cisco RW
!
logging 10.0.0.100
line con 0
!
line aux 0
!
line vty 0 4
 login
!
!
ntp authentication-key 1 md5 0822455D0A16 7
ntp authenticate
ntp trusted-key 1
ntp server 10.0.0.100 key 1
!
end
```
rus-msk-r3:
```
!
version 15.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname R3
!
!
!
enable secret 5 $1$mERr$hx5rVt7rPNoS4wqbXKX7m0
!
!
!
!
!
aaa new-model
!
aaa authentication login TELNET_AUTH group radius local 
!
!
!
!
!
!
!
no ip cef
no ipv6 cef
!
!
!
username newadmin secret 5 $1$mERr$hx5rVt7rPNoS4wqbXKX7m0
!
!
license udi pid CISCO2811/K9 sn FTX10177M0D-
!
!
!
!
!
!
!
!
!
ip domain-name msk.local
!
!
spanning-tree mode pvst
!
!
!
!
!
!
interface Loopback0
 ip address 192.168.103.3 255.255.255.0
!
interface Tunnel0
 ip address 200.200.200.3 255.255.255.0
 mtu 1476
 tunnel source FastEthernet0/0
 tunnel destination 40.40.40.1
!
!
interface FastEthernet0/0
 ip address 10.0.0.3 255.0.0.0
 ip access-group 120 in
 duplex auto
 speed auto
 standby 1 ip 10.0.0.1
 standby 1 preempt
!
interface FastEthernet0/1
 ip address 12.0.0.3 255.0.0.0
 ip access-group 120 in
 duplex auto
 speed auto
!
interface Vlan1
 no ip address
 shutdown
!
router eigrp 100
 network 10.0.0.0
 network 12.0.0.0
!
router rip
 version 2
 network 192.168.103.0
 network 200.200.200.0
 no auto-summary
!
ip classless
!
ip flow-export version 9
!
!
access-list 120 permit icmp any any echo-reply
access-list 120 deny icmp any any echo
access-list 120 permit ip any any
!
banner motd #Rabotu vypolnil Koval' Artem student gruppy 9SA-321, v zhurnale pod nomerom 12!#
!
radius server 10.0.0.100
 address ipv4 10.0.0.100 auth-port 1645
 key cisco
!
!
snmp-server community cisco RW
!
logging 10.0.0.100
line con 0
!
line aux 0
!
line vty 0 4
 login authentication TELNET_AUTH
 transport input telnet
!
!
ntp authentication-key 1 md5 0822455D0A16 7
ntp authenticate
ntp trusted-key 1
ntp server 10.0.0.100 key 1
!
end
```
rus-msk-multisv1:
```
!
version 12.2(37)SE1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname MLS
!
!
!
!
!
!
ip routing
!
!
!
!
!
!
!
!
!
!
!
!
!
!
!
spanning-tree mode pvst
!
!
!
!
!
!
interface FastEthernet0/1
 no switchport
 ip address 11.0.0.50 255.0.0.0
 duplex auto
 speed auto
!
interface FastEthernet0/2
 no switchport
 ip address 12.0.0.50 255.0.0.0
 duplex auto
 speed auto
!
interface FastEthernet0/3
 no switchport
 ip address 40.40.40.50 255.255.255.0
 duplex auto
 speed auto
!
interface FastEthernet0/4
 switchport access vlan 100
 switchport mode access
!
interface FastEthernet0/5
 switchport access vlan 200
 switchport mode access
!
interface FastEthernet0/6
!
interface FastEthernet0/7
!
interface FastEthernet0/8
!
interface FastEthernet0/9
!
interface FastEthernet0/10
!
interface FastEthernet0/11
!
interface FastEthernet0/12
!
interface FastEthernet0/13
!
interface FastEthernet0/14
!
interface FastEthernet0/15
!
interface FastEthernet0/16
!
interface FastEthernet0/17
!
interface FastEthernet0/18
!
interface FastEthernet0/19
!
interface FastEthernet0/20
!
interface FastEthernet0/21
!
interface FastEthernet0/22
!
interface FastEthernet0/23
!
interface FastEthernet0/24
!
interface GigabitEthernet0/1
!
interface GigabitEthernet0/2
!
interface Vlan1
 no ip address
 shutdown
!
interface Vlan100
 mac-address 000c.cf1e.8501
 ip address 100.0.0.50 255.0.0.0
!
interface Vlan200
 mac-address 000c.cf1e.8502
 ip address 200.0.0.50 255.255.255.0
!
router eigrp 100
 network 11.0.0.0
 network 12.0.0.0
 network 40.40.40.0 0.0.0.255
 network 100.0.0.0
 network 200.0.0.0
 no auto-summary
!
ip classless
!
ip flow-export version 9
!
!
!
!
!
!
!
!
line con 0
!
line aux 0
!
line vty 0 4
 login
!
!
!
!
end
```
rus-msk-serv1:

<img width="699" height="268" alt="изображение" src="https://github.com/user-attachments/assets/e0fff3f4-acc0-4aef-9524-cf701456a380" />

rus-msk-pc6:

<img width="690" height="283" alt="изображение" src="https://github.com/user-attachments/assets/45bd7a21-15c5-4ca9-a34d-5cd322c4dc95" />

rus-msk-pc7:

<img width="696" height="288" alt="изображение" src="https://github.com/user-attachments/assets/1bec6722-af45-4e42-9305-0fb83754ae01" />

rus-nsk-pc0:

<img width="692" height="289" alt="изображение" src="https://github.com/user-attachments/assets/0a3acce1-4480-4194-b63f-9ced78a82b08" />

rus-nsk-pc1:

<img width="698" height="295" alt="изображение" src="https://github.com/user-attachments/assets/2cf60693-2893-446e-bb29-c1b8ea1bdd09" />

rus-nsk-pc2:

<img width="685" height="302" alt="изображение" src="https://github.com/user-attachments/assets/603d8b8b-7d2c-4b83-86c6-7cc4ab70e1aa" />

rus-nsk-pc3:

<img width="689" height="291" alt="изображение" src="https://github.com/user-attachments/assets/6c0cdbcd-962f-4a03-979c-97750ea4dd68" />

rus-nsk-pc4:

<img width="692" height="285" alt="изображение" src="https://github.com/user-attachments/assets/7c6e8053-e4e5-4713-87d4-4a17decbfd74" />

rus-nsk-pc5:

<img width="688" height="296" alt="изображение" src="https://github.com/user-attachments/assets/4f7b0339-6edf-4e22-a1b1-2d74a530177b" />








