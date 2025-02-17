# Commandes utilisées dans le lab

## Configuration des interfaces
```plaintext
Router>en
Router#conf t
Router(config)#int g0/0
Router(config-if)#ip add 172.22.34.65 255.255.255.224
Router(config-if)#no sh
Router(config-if)#int g0/1
Router(config-if)#ip add 172.22.34.97 255.255.255.240
Router(config-if)#no sh
Router(config-if)#int g0/2
Router(config-if)#ip add 172.22.34.1 255.255.255.192
Router(config-if)#no sh

```plaintext
## Configuration des ACL

```plaintext
Router(config)#access-list 100 permit tcp 172.22.34.66 0.0.0.31 host 172.22.34.62 eq 21
Router(config)#access-list 100 permit icmp 172.22.34.66 0.0.0.31 host 172.22.34.62
Router(config-if)#ip access-group 100 in


```plaintext 

## Vérification des ACL
```plaintext
Router(config)#do show access-list
```plaintext
