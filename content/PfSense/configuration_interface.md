---
title: "Configuration interface PfSense"
date: 2017-10-17T15:26:15Z
draft: false
weight: 40
description: "Configuration interface PfSense"
---

#### Configurer les interfaces:

- Assigner l'interface **WAN** `em0`:  
![00](/images/pfsense/configuration/assignation/00.PNG)

---

- Selectionner l'option `1`:  
![01](/images/pfsense/configuration/assignation/01.PNG)

---

- Ne pas configurer de VLAN `n`:  
![02](/images/pfsense/configuration/assignation/02.PNG)

---

- **WAN** Selectionner l'interface `em0`:  
![03](/images/pfsense/configuration/assignation/03.PNG)

---

- **LAN** Selectionner l'interface `em1`:  
![04](/images/pfsense/configuration/assignation/04.PNG)

---

- Appuyer sur `entrée` pour finir l'assignation des interfaces **WAN/LAN**
- Saisir `y` pour valider les assignations:  
![05](/images/pfsense/configuration/assignation/05.PNG)

---

- La configuration se termine:  
![06](/images/pfsense/configuration/assignation/06.PNG)

---

#### Définir les adresses IP's:  

##### Définir l'adresse IP WAN:  
```
WAN:
	IP: 192.168.11.2
	MASK: 255.255.255.252
```

- Saisir `2` (Set interface(s) IP address):  
![00](/images/pfsense/configuration/ip/00.PNG)

---

- Saisir `1` pour l'interface **WAN**:  
![01](/images/pfsense/configuration/ip/01.PNG)

---

- Saisir `n` pour définir l'interface **WAN** en statique:  
![02](/images/pfsense/configuration/ip/02.PNG)

---

- Saisir l'IP `192.168.11.2`:  
![03](/images/pfsense/configuration/ip/03.PNG)

---

- Saisir `30` pour le masque de sous réseau:  
![04](/images/pfsense/configuration/ip/04.PNG)

---

- Appuyer sur `entrée`
- Ne pas configurer en DHCP IPv6 
- Ne pas configurer d'adresse IPv6
- Choisir `n` pour ne pas rendre accessible le WebConfigurator depuis le WAN
![05](/images/pfsense/configuration/ip/05.PNG)



##### Définir l'adresse IP LAN:  
```
LAN:
	IP: 192.168.1.1
	MASK: 255.255.255.0
```

- Saisir `2` (Set interface(s) IP address)
- Saisir `2` pour l'interface **LAN**
- Saisir l'IP `192.168.1.1`
- Saisir `24` pour le masque de sous réseau
![06](/images/pfsense/configuration/ip/06.PNG)

---

- Ne pas définir de GW
- Ne pas définir d'IPv6
- Ne pas activer le DHCP
![07](/images/pfsense/configuration/ip/07.PNG)
