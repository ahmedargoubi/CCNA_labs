# Lab : Configuration des pools DHCP et relais DHCP

## Objectif
Ce lab a pour objectif de configurer des pools DHCP sur un routeur (R2) et de configurer un autre routeur (R1) comme client DHCP et relais DHCP. Les PCs (PC1 et PC2) doivent également obtenir des adresses IP via DHCP.

---

## **Topologie**
- **R1** :
  - Interface G0/0 : Client DHCP
  - Interface G0/1 : Relais DHCP pour le réseau `192.168.1.0/24`
- **R2** :
  - Configuration des pools DHCP :
    - POOL1 : `192.168.1.0/24` (réserver `.1` à `.10`)
    - POOL2 : `192.168.2.0/24` (réserver `.1` à `.10`)
    - POOL3 : `203.0.113.0/30` (réserver `.1`)
- **PC1** : Connecté au réseau `192.168.1.0/24`
- **PC2** : Connecté au réseau `192.168.2.0/24`



---

## **Commandes utilisées**
Voir le fichier [COMMANDS.md](COMMANDS.md) pour la liste complète des commandes.

---


