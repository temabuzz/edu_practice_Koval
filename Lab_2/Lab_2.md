# Часть 1

## Шаг 1 - Создание топологии

<img width="1600" height="493" alt="изображение" src="https://github.com/user-attachments/assets/886d96a4-22fd-457f-8e4a-dc2e549bb13f" />

*Рис.1 Создание топологии*

## Шаг 2 - Настройка f0/0-1 на R1

<img width="357" height="86" alt="изображение" src="https://github.com/user-attachments/assets/8dcc2187-8aeb-4c26-b353-aed43e37f87b" />

*Рис.2 Настройка f0/0-1 на R1*

## Шаг 3 - Настройка f0/0-1 на R2

<img width="616" height="243" alt="изображение" src="https://github.com/user-attachments/assets/13c474f8-2fa6-4bf5-95f0-e2da678df6b3" />

*Рис.3 Настройка f0/0-1 на R2*

## Шаг 4 - Настройка loopback, g0/0, s0/0/0

<img width="623" height="419" alt="изображение" src="https://github.com/user-attachments/assets/2ba151a3-3250-4c11-88a0-4988fcfa75f9" />

*Рис.4 Настройка loopback, g0/0, s0/0/0*

## Шаг 5 - Настройка loopback, s0/0/0 на R1973

<img width="586" height="196" alt="изображение" src="https://github.com/user-attachments/assets/ee4ffc0d-5ddf-47e7-95e9-779e5d396d87" />

*Рис.5 Настройка loopback, s0/0/0 на R1973*

# Часть 2

## Шаг 1 - Настройка PPP на R3

<img width="608" height="113" alt="изображение" src="https://github.com/user-attachments/assets/d0e675a4-432e-46e5-be8d-89234476b5e8" />

*Рис.6 Настройка PPP на R3*

## Шаг 2 - Настройка PPP на R1973

<img width="302" height="71" alt="изображение" src="https://github.com/user-attachments/assets/91e45fe3-e834-416c-bc1b-ddaca2a637d0" />

*Рис.7 Настройка PPP на R1973*

# Часть 3

## Шаг 1 - Настройка OSPFv2 на R1, R2, R3

R1:

<img width="190" height="16" alt="изображение" src="https://github.com/user-attachments/assets/454cab6e-bb06-49c8-b50a-90cf21ebde9b" />

*Рис.8 Настройка OSPFv2 на R1*

R2:

<img width="201" height="16" alt="изображение" src="https://github.com/user-attachments/assets/dbfd6a20-3b51-41c2-b5fd-c10136babc7b" />

*Рис.9 Настройка OSPFv2 на R2*

R3:

<img width="191" height="19" alt="изображение" src="https://github.com/user-attachments/assets/b487a081-15cb-434f-8aeb-8df327a58b43" />

*Рис.10 Настройка OSPFv2 на R3*

## Шаг 2 - Настройка Router-id на R2

<img width="259" height="18" alt="изображение" src="https://github.com/user-attachments/assets/f3d3d12a-73d0-446f-8b32-5290cec493b1" />

*Рис.11 Настройка Router-id на R2*

## Шаг 3 - Настройка объявления всех подключений сети на роутерах

R1:

<img width="380" height="28" alt="изображение" src="https://github.com/user-attachments/assets/8c910da6-bbd7-41a2-9878-59f6a04fbb3c" />

*Рис.12 Объявление подключений сети на R1*

R2:

<img width="391" height="27" alt="изображение" src="https://github.com/user-attachments/assets/eb1fabc2-79da-4744-8047-b183c2ecd6af" />

*Рис.13 Объявление подключений сети на R2*

R3:

<img width="403" height="57" alt="изображение" src="https://github.com/user-attachments/assets/7fd8006d-fc02-4667-a132-7cadd0df7453" />

*Рис.14 Объявление подключений сети на R3*

## Шаг 4 - Отключение hello-пакетов на R1, кроме f0/1

<img width="624" height="98" alt="изображение" src="https://github.com/user-attachments/assets/c41bf5a8-09c5-4b22-abb9-d8c2ebe18277" />

*Рис.15 Отключение hello-пакетов на R1, кроме f0/1*

## Шаг 5 - Настройка DR на R2

<img width="253" height="56" alt="изображение" src="https://github.com/user-attachments/assets/5131d9f0-d653-4b1b-b6f7-505956b6c79d" />

*Рис.16 Настройка DR на R2*

## Шаг 6 - Назначение R3 шлюзом по умолчанию для OSPF

<img width="380" height="72" alt="изображение" src="https://github.com/user-attachments/assets/0bf4a9dd-fd72-442c-b319-0d2b6c3ddd82" />

*Рис.17 Назначение R3 шлюзом по умолчанию для OSPF*

# Часть 4

## Шаг 1 - Настройка BGP на R3 и R1973

R3:

<img width="177" height="17" alt="изображение" src="https://github.com/user-attachments/assets/c5b82987-78e3-4b6c-9fdf-105a5e7b67f1" />

*Рис.18 Настройка BGP на R3*

R1973:

<img width="216" height="16" alt="изображение" src="https://github.com/user-attachments/assets/959c8e3e-4cd6-4223-8aa9-608dee120cf6" />

*Рис.19 Настройка BGP на R1973*

## Шаг 2 - Настройка соседства BGP

R3:

<img width="389" height="17" alt="изображение" src="https://github.com/user-attachments/assets/d0dd7398-419d-4eac-896c-83e1467a69e5" />

*Рис.20 Настройка соседства BGP на R3*

R1973:

<img width="375" height="16" alt="изображение" src="https://github.com/user-attachments/assets/cd7919f3-515a-460c-8703-b6c7fed8cc05" />

*Рис.21 Настройка соседства BGP на R1973*

## Шаг 3 - Объявляем loopback

<img width="421" height="14" alt="изображение" src="https://github.com/user-attachments/assets/7a57b005-a3d2-4d66-ad3e-bad18f8e0600" />

*Рис.22 Объявление loopback*

## Шаг 4 - Настройка маршрута по умолчанию

<img width="366" height="17" alt="изображение" src="https://github.com/user-attachments/assets/d6413732-e2d3-4926-9769-35c0443d31bb" />

*Рис.23 Настройка маршрута по умолчанию*

## Шаг 5 - Проверка

<img width="575" height="221" alt="изображение" src="https://github.com/user-attachments/assets/03fe1871-7564-4f12-a7a9-8c620f127d28" />

*Рис.24 Проверка BGP*

# Часть 5

## Шаг 1 - Проверка поддержки лицензии на R3

<img width="445" height="321" alt="изображение" src="https://github.com/user-attachments/assets/7848819b-79c6-4f39-b527-b02b849f450f" />

*Рис.25 Проверка поддержки лицензии на R3*

## Шаг 2 - Установка лицензии UCK9

<img width="425" height="16" alt="изображение" src="https://github.com/user-attachments/assets/fc6c39ed-b8d0-402c-9932-f8b29f166a1d" />

*Рис.26 Установка лицензии UCK9*

Согласие с установкой:

<img width="606" height="99" alt="изображение" src="https://github.com/user-attachments/assets/5f4db886-0f68-4b79-96c2-d5db9d4abf4c" />

*Рис.27 Согласие с установкой лицензии*

## Шаг 3 - Сохранение конфигурации и перезагрузка

<img width="171" height="60" alt="изображение" src="https://github.com/user-attachments/assets/5b365ef5-8326-426c-9209-3433751cc122" />

*Рис.28 Сохранение конфигурации и перезагрузка*

# Часть 6

## Шаг 1 - Настройка R1 в качестве DHCP-ретранслятора

<img width="324" height="29" alt="изображение" src="https://github.com/user-attachments/assets/887a4abe-0fdb-473d-9352-b31ae29aa988" />

*Рис.29 Настройка R1 в качестве DHCP-ретранслятора*

## Шаг 2 - Проверка выдачи IP на PC0

<img width="693" height="293" alt="изображение" src="https://github.com/user-attachments/assets/1fb35bdf-6650-4b36-9f1f-0d01ce47b40b" />

*Рис.30 Проверка выдачи IP на PC0*

# Часть 7

## Шаг 1 - Настройка R1, R2, R3, R1973 с IPv6-адресами

R1:

<img width="372" height="69" alt="изображение" src="https://github.com/user-attachments/assets/16c2f04f-5c69-4a5f-aeda-1223013818e8" />

*Рис.31 Настройка IPv6 на R1*

R2:

<img width="332" height="57" alt="изображение" src="https://github.com/user-attachments/assets/c0a34648-5904-44fc-90fa-ef0ab8c8af13" />

*Рис.32 Настройка IPv6 на R2*

R3:

<img width="343" height="73" alt="изображение" src="https://github.com/user-attachments/assets/8b86b6c2-9fba-433c-9e2f-d89f136678f3" />

*Рис.33 Настройка IPv6 на R3*

R1973:

<img width="424" height="72" alt="изображение" src="https://github.com/user-attachments/assets/6e0034d6-b155-4b86-a87b-96860d139b1f" />

*Рис.34 Настройка IPv6 на R1973*

## Шаг 2 - Включение маршрутизации ipv6

R1:

<img width="231" height="14" alt="изображение" src="https://github.com/user-attachments/assets/037e8493-cdec-4e5c-bd7d-1acb082ca668" />

*Рис.35 Включение маршрутизации IPv6 на R1*

R2:

<img width="228" height="17" alt="изображение" src="https://github.com/user-attachments/assets/8057df09-6e55-45fc-be4a-b111a2ae4ab9" />

*Рис.36 Включение маршрутизации IPv6 на R2*

R3:

<img width="224" height="10" alt="изображение" src="https://github.com/user-attachments/assets/d202b4fe-af44-4b90-b35a-3176e0a2c2a5" />

*Рис.37 Включение маршрутизации IPv6 на R3*

R1973:

<img width="245" height="19" alt="изображение" src="https://github.com/user-attachments/assets/5d31dac4-4b00-4416-b6f9-7c94c8d34790" />

*Рис.38 Включение маршрутизации IPv6 на R1973*

## Шаг 3 - Проверка f0/0 на R1

<img width="420" height="113" alt="изображение" src="https://github.com/user-attachments/assets/e9a76d6e-8eb1-4c9b-8fc3-f07f6ea479ea" />

*Рис.39 Проверка f0/0 на R1*

# Часть 8

## Шаг 1 - Настройка OSPFv3, назначение Router-id на R1, R2, R3

R1:

<img width="239" height="29" alt="изображение" src="https://github.com/user-attachments/assets/aa34fef4-bc51-4dc7-9a3c-77b1b6b6de67" />

*Рис.40 Настройка OSPFv3 и Router-id на R1*

R2:

<img width="238" height="25" alt="изображение" src="https://github.com/user-attachments/assets/5f3d42e5-bcc8-4f35-90c7-ac2f6e2ddce5" />

*Рис.41 Настройка OSPFv3 и Router-id на R2*

R3:

<img width="236" height="30" alt="изображение" src="https://github.com/user-attachments/assets/3f6d5f31-fe66-40be-8090-8950372b8e37" />

*Рис.42 Настройка OSPFv3 и Router-id на R3*

## Шаг 2 - Настройка Area

R1:

<img width="264" height="68" alt="изображение" src="https://github.com/user-attachments/assets/eca7225d-6168-45b6-9225-ba92fa01937a" />

*Рис.43 Настройка Area на R1*

R2:

<img width="261" height="70" alt="изображение" src="https://github.com/user-attachments/assets/cd55e347-bcf9-43d0-bc43-4f412f59129d" />

*Рис.44 Настройка Area на R2*

R3:

<img width="254" height="28" alt="изображение" src="https://github.com/user-attachments/assets/67e841f1-3bd8-41db-8d61-9bc0916b47d3" />

*Рис.45 Настройка Area на R3*

## Шаг 3 - Запрет на Hello-сообщения

<img width="297" height="40" alt="изображение" src="https://github.com/user-attachments/assets/50534773-018a-4ec6-bb15-49d9b3f78167" />

*Рис.46 Запрет на Hello-сообщения*

## Шаг 4 - Настройка R3 как шлюз по умолчанию

<img width="332" height="59" alt="изображение" src="https://github.com/user-attachments/assets/b2ee38bf-da77-4e98-9363-ee19bf704470" />

*Рис.47 Настройка R3 как шлюз по умолчанию*

Проверка:

<img width="579" height="58" alt="изображение" src="https://github.com/user-attachments/assets/43892ba6-289c-4e42-937e-80dec91ee9e9" />

*Рис.48 Проверка шлюза по умолчанию*

# Часть 9

## Шаг 1 - Настройка EIGRPv6 между R3 и R1973

Назначение router-id, объявление loopback, настройка ipv6 маршрут по умолчанию

R3:

<img width="279" height="68" alt="изображение" src="https://github.com/user-attachments/assets/be6eaa7c-e095-4a76-826f-64b7d593a100" />

*Рис.49 Настройка EIGRPv6 на R3*

R1973:

<img width="350" height="110" alt="изображение" src="https://github.com/user-attachments/assets/8d117cff-0e38-42bc-9fbd-20bddd6eb1d2" />

*Рис.50 Настройка EIGRPv6 на R1973*

## Шаг 2 - Проверка на R3

<img width="559" height="120" alt="изображение" src="https://github.com/user-attachments/assets/883f489b-f91e-45a5-a46f-36ca22b1892c" />

*Рис.51 Проверка EIGRPv6 на R3*

# Полная конфигурация
SW0:
```
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname Switch
!
!
!
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
R1:
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
!
!
!
!
ip cef
ipv6 unicast-routing
!
no ipv6 cef
!
!
!
!
license udi pid CISCO2811/K9 sn FTX1017902J-
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
interface FastEthernet0/0
 ip address 10.1.1.1 255.255.255.0
 ip helper-address 10.23.23.100
 duplex auto
 speed auto
 ipv6 address FE80::1 link-local
 ipv6 address 2001:10:10:10::/64 eui-64
 ipv6 ospf 100 area 1
!
interface FastEthernet0/1
 ip address 10.12.12.1 255.255.255.0
 duplex auto
 speed auto
 ipv6 address 2001:11:11:11::1/64
 ipv6 ospf 100 area 0
!
interface Vlan1
 no ip address
 shutdown
!
router ospf 100
 log-adjacency-changes
 passive-interface default
 no passive-interface FastEthernet0/1
 network 10.1.1.0 0.0.0.255 area 1
 network 10.12.12.0 0.0.0.255 area 0
!
ipv6 router ospf 100
 router-id 0.0.0.1
 log-adjacency-changes
 passive-interface default
 no passive-interface FastEthernet0/1
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
line con 0
!
line aux 0
!
line vty 0 4
 login
!
!
!
end
```
R2:
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
ip cef
ipv6 unicast-routing
!
no ipv6 cef
!
!
!
!
license udi pid CISCO2811/K9 sn FTX1017H8DT-
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
interface FastEthernet0/0
 ip address 10.23.23.2 255.255.255.0
 ip ospf priority 255
 duplex auto
 speed auto
 ipv6 address 2001:12:12:12::2/64
 ipv6 ospf 100 area 23
!
interface FastEthernet0/1
 ip address 10.12.12.2 255.255.255.0
 ip ospf priority 255
 duplex auto
 speed auto
 ipv6 address 2001:11:11:11::2/64
 ipv6 ospf 100 area 0
!
interface Vlan1
 no ip address
 shutdown
!
router ospf 100
 router-id 0.0.0.2
 log-adjacency-changes
 network 10.12.12.0 0.0.0.255 area 0
 network 10.23.23.0 0.0.0.255 area 23
!
ipv6 router ospf 100
 router-id 0.0.0.2
 log-adjacency-changes
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
line con 0
!
line aux 0
!
line vty 0 4
 login
!
!
!
end
```
R3:
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
!
!
!
!
!
no ip cef
ipv6 unicast-routing
!
no ipv6 cef
!
!
!
username R1973 password 0 cisco
!
!
license udi pid CISCO2911/K9 sn FTX1524GPBT-
license boot module c2900 technology-package securityk9
license boot module c2900 technology-package uck9
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
interface Loopback3
 ip address 3.3.3.3 255.0.0.0
!
interface Loopback33
 ip address 33.33.33.33 255.0.0.0
!
interface GigabitEthernet0/0
 ip address 10.23.23.3 255.255.255.0
 duplex auto
 speed auto
 ipv6 address 2001:12:12:12::3/64
 ipv6 ospf 100 area 23
!
interface GigabitEthernet0/1
 no ip address
 duplex auto
 speed auto
 shutdown
!
interface GigabitEthernet0/2
 no ip address
 duplex auto
 speed auto
 shutdown
!
interface Serial0/0/0
 ip address 30.30.30.3 255.255.255.0
 encapsulation ppp
 ppp authentication chap
 ppp chap hostname R3
 ipv6 address 2001:30:30:30::3/64
 ipv6 eigrp 100
 clock rate 2000000
!
interface Serial0/0/1
 no ip address
 clock rate 2000000
 shutdown
!
interface Vlan1
 no ip address
 shutdown
!
router ospf 100
 log-adjacency-changes
 network 3.0.0.0 0.255.255.255 area 23
 network 33.0.0.0 0.255.255.255 area 23
 network 10.23.23.0 0.0.0.255 area 23
 default-information originate
!
router bgp 3
 bgp log-neighbor-changes
 no synchronization
 neighbor 30.30.30.73 remote-as 1973
!
ipv6 router ospf 100
 router-id 0.0.0.3
 default-information originate
 log-adjacency-changes
!
ipv6 router eigrp 100
 eigrp router-id 0.0.0.3
 no shutdown 
!
ip classless
ip route 0.0.0.0 0.0.0.0 30.30.30.73 
!
ip flow-export version 9
!
ipv6 route ::/0 2001:30:30:30::1973
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
end
```
R1973:
```
!
version 15.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname R1973
!
!
!
!
!
!
!
!
no ip cef
ipv6 unicast-routing
!
no ipv6 cef
!
!
!
username R3 password 0 cisco
!
!
license udi pid CISCO2911/K9 sn FTX15240CO3-
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
interface Loopback1973
 ip address 73.73.73.73 255.255.255.0
 ipv6 address 2001:1973:1973:1973::1973/64
 ipv6 eigrp 100
!
interface GigabitEthernet0/0
 no ip address
 duplex auto
 speed auto
 shutdown
!
interface GigabitEthernet0/1
 no ip address
 duplex auto
 speed auto
 shutdown
!
interface GigabitEthernet0/2
 no ip address
 duplex auto
 speed auto
 shutdown
!
interface Serial0/0/0
 ip address 30.30.30.73 255.255.255.0
 encapsulation ppp
 ppp authentication chap
 ppp chap hostname R1973
 ipv6 address 2001:30:30:30::1973/64
 ipv6 eigrp 100
!
interface Serial0/0/1
 no ip address
 clock rate 2000000
 shutdown
!
interface Vlan1
 no ip address
 shutdown
!
router bgp 1973
 bgp log-neighbor-changes
 no synchronization
 neighbor 30.30.30.3 remote-as 3
 network 73.73.73.0 mask 255.255.255.0
!
ipv6 router eigrp 100
 eigrp router-id 0.0.0.73
 no shutdown 
!
ip classless
ip route 0.0.0.0 0.0.0.0 30.30.30.3 
!
ip flow-export version 9
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
end
```
MLS:
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
DHCP-Server:

<img width="689" height="457" alt="изображение" src="https://github.com/user-attachments/assets/393c3032-6571-4f2a-93ad-1f7d9a5ac966" />


<img width="685" height="282" alt="изображение" src="https://github.com/user-attachments/assets/d5721674-856c-43f8-b3cb-bb67e03781af" />

PC0:

<img width="689" height="292" alt="изображение" src="https://github.com/user-attachments/assets/9dc5fb60-c9d6-43ab-ac4c-45e49c143166" />






