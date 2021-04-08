---
title: "Port Forwarding pour serveur TFTP"
date: 2017-10-17T15:26:15Z
draft: false
weight: 11
description: "Création d'un Port Forwarding pour pouvoir récupérer la configuration du routeur à traver un réseau NATé"
---


**Objectif:** Récupérer la configuration du routeur `RTROUT` depuis le réseau local qui lui est NATé par le PfSense

- Créer la route depuis le routeur `RTROUT`:  
```bash  
192.168.1.0 255.255.255.0 192.168.11.2
```

- Créer la règle de Port Forwarding sur l'interface `WAN` pour autoriser le protocole TFTP qui utilise le port 69:  
![00](/images/tftp_forwarding/00.png)

- Voici la configuration:  
![01](/images/tftp_forwarding/01.png)
![02](/images/tftp_forwarding/02.png)

- Désactiver le blocage des adresses IP publique 
![03](/images/tftp_forwarding/03.PNG)