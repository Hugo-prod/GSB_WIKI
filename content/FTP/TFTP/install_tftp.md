---
title: "Installation du serveur TFTP"
date: 2017-10-17T15:26:15Z
draft: false
weight: 10
description: "Installation du serveur TFTP"
---

- Installation du package `tftpd-hpa`:
```bash  
sudo apt-get install tftpd-hpa
```

- Fichier de configuration `/etc/default/tftpd-hpa`:
```bash
# /etc/default/tftpd-hpa
TFTP_USERNAME="tftp"
TFTP_DIRECTORY="/home/sio/upload/tftp/"
TFTP_ADDRESS=":69"
TFTP_OPTIONS="--secure --create"
```

- Créer le dossier `/home/sio/upload/tftp/`:
```bash
mkdir /home/sio/upload/tftp/
```

- Changer le propriétaire et le groupe du dossier:
```bash  
cd /home/sio/upload/
chown tftp:tftp tftp/
```

- relancer le service (Charger la nouvelle conf):
```bash  
systemctl restart tftpd-hpa
```
