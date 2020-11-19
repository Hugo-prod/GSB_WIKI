---
title: "Adressage IP/Interface"
date: 2017-10-17T15:26:15Z
draft: false
weight: 10
description: "Adressage IP/Interface"
---

Feuille GSheet: [Lien](https://docs.google.com/spreadsheets/d/1ivqRhIszc4veoKZmCXfU5Y8Um4q_rQ7lHaY-grSesEw/edit?usp=sharing)

|Périphérique               |IP          |Masque         |CIDR|Gateway|Port sortant|Port entrant|Périphérique     |Flux                                           |
|---------------------------|------------|---------------|----|-------|------------|------------|-----------------|-----------------------------------------------|
|                           |            |               |    |       |            |            |                 |                                               |
|ROUTER CISCO               |192.168.10.2|255.255.255.252|/30 |       |G0/0        |???         |???              |ROUTER <-> WAN                                 |
|ROUTER CISCO               |192.168.11.1|255.255.255.252|/30 |       |G0/1        |ENO1        |PROXMOX (PFSENSE)|ROUTER <-> PROXMOX (PFSENSE)                   |
|                           |            |               |    |       |            |            |                 |                                               |
|PROXMOX (PFSENSE)          |192.168.11.2|255.255.255.252|/30 |       |ENO1        |G0/1        |ROUTEUR CISCO    |PROXMOX (PFSENSE) <-> ROUTER CISCO             |
|PROXMOX (PFSENSE)          |192.168.1.1 |255.255.255.0  |/24 |       |ENO2        |F0/0        |SWITCH (MUTLAB)  |PROXMOX (PFSENSE) <-> SWITCH (MUTLAB)          |
|                           |            |               |    |       |            |            |                 |                                               |
|PROXMOX (DHCP WINDOWS)     |192.168.1.2 |255.255.255.0  |/24 |       |ENO2        |F0/1        |SWITCH (MUTLAB)  |PROXMOX (DHCP WINDOWS) <-> SWITCH (MUTLAB)     |
|___ (DHCP LINUX REDUNDANCY)|192.168.1.3 |255.255.255.0  |/24 |       |enp0s3      |F0/2        |SWITCH (MUTLAB)  |___ (DHCP LINUX REDUNDANCY) <-> SWITCH (MUTLAB)|
|                           |            |               |    |       |            |            |                 |                                               |
|PROXMOX (DNS WINDOWS)      |192.168.1.2 |255.255.255.0  |/24 |       |ENO2        |F0/1        |SWITCH (MUTLAB)  |PROXMOX (DNS WINDOWS) <-> SWITCH (MUTLAB)      |
|___(DNS LINUX REDUNDANCY)  |192.168.1.4 |255.255.255.0  |/24 |       |enp0s3      |F0/3        |SWITCH (MUTLAB)  |___(DNS LINUX REDUNDANCY) <-> SWITCH (MUTLAB)  |
|                           |            |               |    |       |            |            |                 |                                               |
|PROXMOX (AD WINDOWS)       |192.168.1.2 |255.255.255.0  |/24 |       |ENO2        |F0/1        |SWITCH (MUTLAB)  |PROXMOX (AD WINDOWS) <-> SWITCH (MUTLAB)       |
|                           |            |               |    |       |            |            |                 |                                               |
|DELL DEBIAN SERVER FTP     |192.168.1.5 |255.255.255.0  |/24 |       |enp0s3      |F0/4        |SWITCH (MUTLAB)  |DELL DEBIAN SERVER FTP <-> SWITCH (MUTLAB)     |
|                           |            |               |    |       |            |            |                 |                                               |
|NUC (WINDOWS)              |192.168.1.10|255.255.255.0  |/24 |       |ethernet    |F0/5        |SWITCH (MUTLAB)  |NUC (WINDOWS) <-> SWITCH (MUTLAB)              |
|NUC (LINUX)                |192.168.1.11|255.255.255.0  |/24 |       |enp0s3      |F0/6        |SWITCH (MUTLAB)  |NUC (LINUX) <-> SWITCH (MUTLAB)                |
