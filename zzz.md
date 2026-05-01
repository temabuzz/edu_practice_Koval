hostname rus-msk-r1

interface f0/0.2
encapsulation dot1Q 2
ip address 2.0.0.1 255.0.0.0

interface f0/0.3
encapsulation dot1Q 3
ip address 3.0.0.1 255.0.0.0

interface f0/0.4
encapsulation dot1Q 4
ip address 4.0.0.1 255.0.0.0

interface f0/1
ip address 40.40.40.1 255.255.255.0
no shutdown

interface loopback1
ip address 192.168.101.1 255.255.255.0

interface tunnel1
ip address 200.200.200.1 255.255.255.0
tunnel source f0/1
tunnel destination 40.40.40.50

router eigrp 100
no auto-summary
network 1.0.0.0
network 2.0.0.0
network 3.0.0.0
network 4.0.0.0
network 40.40.40.0

router rip
version 2
no auto-summary
network 192.168.101.0
network 200.200.200.0

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

ntp authentication-key 1 md5 cisco
ntp authenticate
ntp trusted-key 1
ntp server 10.0.0.100 key 1
