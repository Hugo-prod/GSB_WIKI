---
title: "4. Installer FusionInventory"
date: 2017-10-17T15:26:15Z
draft: false
weight: 40
description: "4. Installer FusionInventory"
---

#### Télécharger FusionInventory (pour GLPI 9.5):

- Téléchargez FusionInventory:  
```bash
wget https://github.com/fusioninventory/fusioninventory-for-glpi/archive/refs/tags/glpi9.5+2.0.zip
```
![00](/images/GLPI/FusionInventory/00.PNG)

- Décompressez FusionInventory:
```bash  
unzip glpi9.5+2.0.zip
``` 

- Copiez FusionInventory dans le repertoire de `/var/www/glpi/plugins/`:
```bash  
cp -r fusioninventory-for-glpi9.5-2.0/ /var/www/glpi/plugins/
```

- Changez les droits du dossier:  
```bash
chown -R www-data fusioninventory-for-glpi9.5-2.0/
```

- Renommez le dossier:
```bash  
mv fusioninventory-for-glpi9.5-2.0/ fusioninventory
```

#### Installer FusionInventory:

- Allez dans les plugins:  
![01](/images/GLPI/FusionInventory/01.PNG)

- Cliquez sur installer:    
![02](/images/GLPI/FusionInventory/02.PNG)

- Installation en cours:  
![03](/images/GLPI/FusionInventory/03.PNG)

- Activez le plugin:  
![04](/images/GLPI/FusionInventory/04.PNG)

- Le plugin est maintenant activé:    
![05](/images/GLPI/FusionInventory/05.PNG)

#### Activer la tache cron:

- Avec l'utilisateur **root**:
```bash  
crontab -u www-data -e
```

- Selectionnez l'éditeur souhaité (Ex:1)

- Ajoutez à la fin du fichier:
```bash  
*/1 * * * * /usr/bin/php5 /var/www/html/glpi/front/cron.php &>/dev/null
```

- Redémarrez le service:
```bash  
/etc/init.d/cron restart
```

- Allez dans `Configuration > Actions Automatiques`:  
![06](/images/GLPI/FusionInventory/06.PNG)

- Cliquez sur TaskScheduler:  
![07](/images/GLPI/FusionInventory/07.PNG)

- Puis cliquez sur executer:   
![08](/images/GLPI/FusionInventory/08.PNG)
