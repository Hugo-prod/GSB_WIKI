---
title: "Configuration SSH"
date: 2017-10-17T15:26:15Z
draft: false
weight: 10
---


- Télécharger la clef privée: [GSB](/SSH/gsb) 
- Télécharger la clef publique: [GSB](/SSH/gsb.pub) 

#### Voici la configuration SSH à ajouter dans le `~/.ssh/config`:
```bash  
###########################
########### GSB ###########
###########################

Host debian-ftp
	Hostname 192.168.1.5
	User root
	IdentityFile ~/.ssh/gsb 

Host glpi
	Hostname 192.168.1.8
	User root
	IdentityFile ~/.ssh/gsb 

Host proxmox
	Hostname 192.168.1.2
	User root
	IdentityFile ~/.ssh/gsb 

Host proxmox_backup
	Hostname 192.168.1.6
	User root
	IdentityFile ~/.ssh/gsb 

Host proxmox_vm_backup
	Hostname 192.168.1.9
	User root
	IdentityFile ~/.ssh/gsb 
```

