# Router Configurations

## R1
```
interface g0/0
 ip address 10.1.1.1 255.255.255.0
 no shutdown
!
interface g0/1
 ip address 192.168.1.1 255.255.255.0
 no shutdown
!
interface g0/2
 ip address 192.168.3.1 255.255.255.0
 no shutdown
!
ip route 192.168.2.0 255.255.255.0 10.1.1.2
ip route 192.168.3.0 255.255.255.0 10.1.1.2
```

## R2
```
interface g0/0
 ip address 10.1.1.2 255.255.255.0
 no shutdown
!
interface g0/1
 ip address 10.2.2.1 255.255.255.0
 no shutdown
!
interface g0/2
 ip address 192.168.2.1 255.255.255.0
 no shutdown
!
ip route 192.168.3.0 255.255.255.0 10.3.3.2
ip route 192.168.1.0 255.255.255.0 10.1.1.1
```

## R3
```
interface g0/0
 ip address 10.3.3.1 255.255.255.0
 no shutdown
!
interface g0/1
 ip address 192.168.2.2 255.255.255.0
 no shutdown
!
interface g0/2
 ip address 192.168.3.2 255.255.255.0
 no shutdown
!
ip route 192.168.1.0 255.255.255.0 10.3.3.1
ip route 192.168.2.0 255.255.255.0 10.3.3.1
```
