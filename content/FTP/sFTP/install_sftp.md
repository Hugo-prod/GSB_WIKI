---
title: "Installation du serveur sFTP"
date: 2017-10-17T15:26:15Z
draft: false
weight: 10
description: "Installation du serveur sFTP"
---

Construction d'un SFTP SSH JAIL

---

- Créer le groupe pour les utilisateurs SFTP:
```bash  
groupadd sftp_users
```

- Ajouter un utilisateur au groupe `sftp_users`:
```bash  
useradd -m -G sftp_users sio
```
- Pour ajouter des utilisateurs existant:
```bash  
usermod -G sftp_users john
```

- Définir le PWD de l'utilisateur:
```bash  
echo "sio:sio2020" | chpasswd
```

- Paramètrer les permissions:
```bash  
chown root /home/sio
```

- Créer un dossier `upload/` dans le dossier de l'utilisateur et paramètrer les permissions:
```bash
mkdir /home/sio/upload
chown sio /home/sio/upload
```

- Editer le fichier de configuration du service SSH `/etc/ssh/sshd_config`:
```bash
#Subsystem      sftp    /usr/lib/openssh/sftp-server
Subsystem       sftp    internal-sftp

Match Group sftp_users
  X11Forwarding no
  AllowTcpForwarding no
  ChrootDirectory %h
  ForceCommand internal-sftp
```

- Redemarrer le service sshd:
```bash  
systemctl restart sshd 
```