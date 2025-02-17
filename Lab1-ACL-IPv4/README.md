# Packet Tracer - Configurer les listes de contrôle d'accès IPv4 étendues (Scenario 1)

## Objectif
Ce lab a pour objectif de configurer des listes de contrôle d'accès (ACL) IPv4 étendues sur un routeur Cisco pour filtrer le trafic réseau.

## **Topologie**
- **Routeur** : 1 routeur Cisco avec 3 interfaces GigabitEthernet (G0/0, G0/1, G0/2).
- **Adressage IP** :
  - G0/0 : 172.22.34.65/27 (masque : 255.255.255.224)
  - G0/1 : 172.22.34.97/28 (masque : 255.255.255.240)
  - G0/2 : 172.22.34.1/26 (masque : 255.255.255.192)
- **PC1** : 172.22.34.66/27 (masque : 255.255.255.224)
- **PC2** : 172.22.34.98/28 (masque : 255.255.255.240)
- **Serveur** : 172.22.34.62/26 (masque : 255.255.255.192)
## Étapes de configuration
1. Configuration des interfaces du routeur.
2. Création des ACL étendues pour filtrer le trafic.
3. Application des ACL sur les interfaces appropriées.

## Commandes utilisées
Voir le fichier [COMMANDS.md](COMMANDS.md) pour la liste complète des commandes.

## Résultats
- ACL 100 appliquée sur G0/0 pour filtrer le trafic FTP et ICMP.
- ACL HTTP appliquée sur G0/1 pour filtrer le trafic HTTP et ICMP.

---
