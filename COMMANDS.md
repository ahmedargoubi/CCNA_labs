# Commandes utilisées dans le lab DHCP

## Sur R2
### Exclure les adresses réservées
```
ip dhcp excluded-address 192.168.1.1 192.168.1.10
ip dhcp excluded-address 192.168.2.1 192.168.2.10
ip dhcp excluded-address 203.0.113.1
ip dhcp pool pool1
 network 192.168.1.0 255.255.255.0
 default-router 192.168.1.1
 dns-server 8.8.8.8
 domain-name ahmed.com
ip dhcp pool pool2
 network 192.168.2.0 255.255.255.0
 default-router 192.168.2.1
 dns-server 8.8.8.8
 domain-name ahmed.com
ip dhcp pool pool3
 network 203.0.113.0 255.255.255.252
 default-router 203.0.113.1
```
## Sur R1
### Configurer l'interface G0/0 comme client DHCP

```
interface GigabitEthernet0/0
 ip address dhcp
 no sh
```
### Configurer l'interface G0/1 comme relais DHCP

```
interface GigabitEthernet0/1
 ip address 192.168.1.1 255.255.255.0
 ip helper-address 203.0.113.1
 no sh
```
### Ajouter une route statique
```

ip route 203.0.113.0 255.255.255.252 203.0.113.1
```
