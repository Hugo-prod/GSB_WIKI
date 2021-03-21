---
title: "3. Installation et configuration GLPI"
date: 2017-10-17T15:26:15Z
draft: false
weight: 30
description: "3. Installation et configuration GLPI"
---


#### Télécharger GLPI:

- Télécharger GLPI:
```bash
cd /tmp
wget https://github.com/glpi-project/glpi/releases/download/9.5.2/glpi-9.5.2.tgz
```
![00](/images/GLPI/GLPI/00.PNG)


- Décompresser GLPI:
```bash
tar -xvzf glpi-9.5.2.tgz
```

- Créer le dossier GLPI:
```bash
mkdir /var/www/glpi
```

- Copier le contenu du dossier GLPI dans `/var/www/glpi`:
```bash
cp -r glpi/* /var/www/glpi
```

- Changer les droits en `www-data`:  
```bash
chown -R www-data /var/www/glpi
```

#### Installation GLPI:

- Selection du langage:
![01](/images/GLPI/GLPI/01.PNG)

- Accepter les termes de la licence:
![02](/images/GLPI/GLPI/02.PNG)

- Installation de GLPI:
![03](/images/GLPI/GLPI/03.PNG)

- Pré-requis et dependances pour l'installation de GLPI:
![04](/images/GLPI/GLPI/04.PNG)
![05](/images/GLPI/GLPI/05.PNG)

- Paramètres de connexion à la base de données:
![06](/images/GLPI/GLPI/06.PNG)

- Selection de la base de données (créée en amont):
![07](/images/GLPI/GLPI/07.PNG)

- Initialisation:
![08](/images/GLPI/GLPI/08.PNG)

- La base de données a bien été initialisée:
![09](/images/GLPI/GLPI/09.PNG)

- Ne pas envoyer des statistique d'usage: 
![10](/images/GLPI/GLPI/10.PNG)

- Installation terminée et identifiants par defaut:  
![11](/images/GLPI/GLPI/11.PNG)

- Connexion à GLPI:
![12](/images/GLPI/GLPI/12.PNG)

- Interface GLPI: 
![13](/images/GLPI/GLPI/13.PNG)

- Supprimer le fichier d'installation:
```bash 
rm /var/www/glpi/install/install.php
```