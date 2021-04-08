---
title: "WiFi (PfSense: Vlan, Interface, Règle FW...)"
date: 2017-10-17T15:26:15Z
draft: false
weight: 30
---

Ici nous allons configurer le VLAN pour le Wifi, définir son interface et créer une règle de Firewall

- Créer le VLAN 130:  
![00](/images/WiFi/wifi_pfsense/00.PNG)

- Associer le VLAN à l'interface (LAN):
![01](/images/WiFi/wifi_pfsense/01.PNG)

- Valider:
![02](/images/WiFi/wifi_pfsense/02.PNG)

- Configurer `OPT1`:  
![03](/images/WiFi/wifi_pfsense/03.PNG)

- Renommer en `WIFI` puis IP statique:  
![04](/images/WiFi/wifi_pfsense/04.PNG)
![05](/images/WiFi/wifi_pfsense/05.PNG)

- Configurer les règles de FireWall:
![06](/images/WiFi/wifi_pfsense/06.PNG)
![07](/images/WiFi/wifi_pfsense/07.PNG)