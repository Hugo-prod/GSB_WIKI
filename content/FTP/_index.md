---
title: "Serveur FTP (sFTP + TFTP)"
date: 2017-10-17T15:26:15Z
draft: false
weight: 10
description: "Documentation du serveur FTP (sFTP + TFTP)"
---

**Description du serveur:**  
L'objectif de ce serveur "FTP" est de proposer un service de stockage pour:  
- Fichier configurations (Routeur/Switch)
- Images .ISO (Windows 7 Pro, Debian, Pfsense ...)

![Serveur FTP](/images/ftp/FTP_SERVER.jpg)


**Informations:**
- ID: `sio`
- PWD: `sio2020`
- IP: `192.168.1.5`

```Bash  
# /etc/network/interfaces
allow-hotplug enp0s3
iface enp0s3 inet static
    address 192.168.1.5 
    netmask 255.255.255.0
    gateway 192.168.1.1
```

---  

#### Documentation:  
- Serveur sFTP:
	- [Installation du serveur sFTP](/ftp/sftp/install_sftp/)
	- [Utilisation du serveur sFTP](/ftp/sftp/use_sftp/)
- Serveur TFTP:
	- [Installation du serveur TFTP](/ftp/tftp/install_tftp/)
	- [Utilisation du serveur TFTP](/ftp/tftp/use_tftp/)