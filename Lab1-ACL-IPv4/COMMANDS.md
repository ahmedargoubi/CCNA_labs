# Commandes utilisées dans le lab

## Configuration des interfaces

### Interface GigabitEthernet0/0
```
Router>en
Router#conf t
Router(config)#int g0/0
Router(config-if)#ip add 172.22.34.65 255.255.255.224
Router(config-if)#no sh
```


### Interface GigabitEthernet0/1
```
Router(config-if)#int g0/1
Router(config-if)#ip add 172.22.34.97 255.255.255.240
Router(config-if)#no sh
```
### Interface GigabitEthernet0/2
```
Router(config-if)#int g0/2
Router(config-if)#ip add 172.22.34.1 255.255.255.192
Router(config-if)#no sh
```
## Configuration des ACL
### Création de l'ACL 100
```
Router(config)#access-list 100 permit tcp 172.22.34.66 0.0.0.31 host 172.22.34.62 eq 21
Router(config)#access-list 100 permit icmp 172.22.34.66 0.0.0.31 host 172.22.34.62
```
### Application de l'ACL sur l'interface GigabitEthernet0/0
```
Router(config-if)#int g0/0
Router(config-if)#ip access-group 100 in
```
### Vérification des ACL
```
Router(config)#do show access-list
```

### Configuration de l'ACL HTTP
```
Router(config)#ip access-list extended HTTP
Router(config-ext-nacl)#permit tcp 172.22.34.98 0.0.0.15 host 172.22.34.62 eq www
Router(config-ext-nacl)#permit icmp 172.22.34.98 0.0.0.15 host 172.22.34.62
Router(config-if)#ip access-group HTTP in
```

### Vérification finale
```
Router(config)#do show access-list
```
