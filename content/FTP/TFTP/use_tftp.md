---
title: "Utilisation du serveur TFTP"
date: 2017-10-17T15:26:15Z
draft: false
weight: 10
description: "Utilisation du serveur TFTP"
---

- Se connecter en TFTP:
```bash  
tftp 192.168.1.5
```

- Activer le mode verbeux:
```bash
tftp> verbose
```

- Téléverser un fichier:
```bash  
tftp> put cisco.cfg
```

- Télécharger un fichier:
```bash  
tftp> get cisco.cfg
```

- Quitter la session TFTP:
```bash  
tftp> quit
```