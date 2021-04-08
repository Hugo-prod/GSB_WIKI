---
title: "2. Installation et configuration serveur, base de données"
date: 2017-10-17T15:26:15Z
draft: false
weight: 20
description: "2. Installation et configuration serveur, base de données"
---


#### Installation des composants LAMP et dépendances pour PHP pour GLPI:  

- Installation des composants LAMP:
```bash  
apt install apache2 php libapache2-mod-php mariadb-server
```

- Installer toutes les dépendances que nous pourrions avoir besoin pour GLPI:
```bash 
apt install php-mysqli php-mbstring php-curl php-gd php-simplexml php-intl php-ldap php-apcu php-xmlrpc php-cas php-zip php-bz2 php-ldap php-imap 
```
---


#### Sécurisation de la DB
- Sécurisez la DB:
```bash 
mysql_secure_installation
```
- Entrez le password **root**:  
![00](/images/GLPI/mysql_secure_installation/00.PNG)

- Changez le password **root**:  
![01](/images/GLPI/mysql_secure_installation/01.PNG)

- Mettre Yes pour tout (Suppression des utilisateurs anonyme, suppression de la DB de test...):  
![02](/images/GLPI/mysql_secure_installation/02.PNG)

- Rechargez les privilèges:  
![03](/images/GLPI/mysql_secure_installation/03.PNG)


---

#### Création de la BD pour GLPI:

- Se connectez à **MySQL** en **root**:
```bash  
mysql -u root
```

- Création de la base de données:
```bash
create database db_glpi;
```

- Création d'un SuperUser pour la base de données GLPI:
```bash
grant all privileges on db_glpi.* to admindb_glpi@localhost identified by "password";
exit
```

---

#### Paramètre du site pour Apache2:

- Faire une copie du fichier `/etc/apache2/sites-available/000-default.conf`:
```bash  
cp /etc/apache2/sites-available/000-default.conf /etc/apache2/sites-available/GLPI.conf
```

- Suppression du site par defaut:
```bash 
rm /etc/apache2/sites-enabled/000-default.conf
```
- Faire un lien symbolique:
```bash 
ln -s /etc/apache2/sites-available/GLPI.conf /etc/apache2/sites-enabled/GLPI.conf
```

- Paramétrez le site dans le fichier `/etc/apache2/sites-available/GLPI.conf` : 
```bash
DocumentRoot /var/www/glpi
<Directory /var/www/glpi>
Options Indexes FollowSymLinks
AllowOverride All
Require all granted
</Directory>
```

![00](/images/GLPI/Apache_conf/00.PNG)

- Redémarrez le service Apache2:  
```Bash
service apache2 restart
```
