---
title: "VLANs"
date: 2017-10-17T15:26:15Z
draft: false
weight: 11
description: "Plan des VLANs"
---


| N° VLAN | VLAN NAME            |                     SERVICE(s)                      |   ADRESSAGE IP   |  CIDR  |      MASQUE       |
| ------- | -------------------- |:---------------------------------------------------:|:----------------:|:------:|:-----------------:|
| ~~10~~  | ~~XXXXXXXXX~~        |       **RESERVEE: Arrivée réseau salle SIO**        | ~~XXXXXXXXXXXX~~ | ~~XX~~ | ~~XXXXXXXXXXXXX~~ |
| 20      | RESEAU_SYSTEME       |                   Réseau & Sytème                   |   192.168.20.0   |   24   |   255.255.255.0   |
| 30      | DIRECTION_DSI        |                   Direction / DSI                   |   192.168.30.0   |   24   |   255.255.255.0   |
| 40      | RH_C_J_SA            | RH / Compta / Juridique / Secrétariat Administratif |   192.168.40.0   |   24   |   255.255.255.0   |
| 50      | COMMUNICATION_REDACT |              Communication / Rédaction              |   192.168.50.0   |   24   |   255.255.255.0   |
| 60      | DEVELOPPEMENT        |                    Développement                    |   192.168.60.0   |   24   |   255.255.255.0   |
| 70      | COMMERCIAL           |                     Commercial                      |   192.168.70.0   |   24   |   255.255.255.0   |
| 80      | LABO_RECHERCHE       |                   Labo-Recherche                    |   192.168.80.0   |   24   |   255.255.255.0   |
| 100     | ACCUEIL              |                       Accueil                       |  192.168.100.0   |   24   |   255.255.255.0   |
| 150     | VISITEUR             |                      Visiteur                       |  192.168.150.0   |   24   |   255.255.255.0   |
| 200     | DEMONSTRATION        |                    Démonstration                    |  192.168.200.0   |   24   |   255.255.255.0   |
| 300     | SERVEURS             |                      Serveurs                       |    172.16.0.0    |   17   |   255.255.128.0   |
| 400     | SORTIE               |                       Sortie                        |    172.18.0.0    |   30   |  255.255.255.252  |
