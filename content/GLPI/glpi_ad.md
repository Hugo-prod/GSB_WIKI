---
title: "5. Lier L'Active Directory à GLPI"
date: 2017-10-17T15:26:15Z
draft: false
weight: 60
description: "5. Lier L'Active Directory à GLPI"
---

- Aller dans Configuration > Authentification:  
![00](/images/GLPI/GLPI_AD/00.PNG)

- Choisissez **Annuaires LDAP**:  
![01](/images/GLPI/GLPI_AD/01.PNG)

- Cliquez sur le **+**:  
![02](/images/GLPI/GLPI_AD/02.PNG)

- Saisir les informations, cliquez sur la préconfiguration **Active directory**:   
![03](/images/GLPI/GLPI_AD/03.PNG)

- **Nom:** Entrez un nom pour reconnaître votre servuer LDAP/AD (ex : SRV-DC01)
- **Serveur par défaut:** Dans le cas de plusieurs serveurs LDAP/AD, celui-ci sera utilisé en priorité
- **Actif:** permet d’activer / désactiver un serveur
- **Serveur:** Entrer l’adresse IP de votre serveur ou le nom de forme serveur.mycompagny.local
- **Port:** Active Directory utilise le port 389 par défaut. Il est possible d’utiliser l’accès en LDAPS en configurant le port 636
- **Filtre de connexion:** Condition permettant de filtrer la recherche des enregistrements (ex : (objectclass=inetOrgPerson)  )
	Vous pouvez utiliser ce filtre (avec Active Directory) pour ne renvoyer que les utilisateurs non désactivés : (&(objectClass=user)(objectCategory=person)(!(userAccountControl:1.2.840.113556.1.4.803:=2)))
- **BaseDN:** emplacement de l’annuaire à partir duquelles les recherches et lectures sont effectuées (sous la forme DC=mycompany,DC=local pour le domaine mycompagny.local) (Utiliser un autre ID que `glpi`)
- **DN du compte:** emplacement du compte à utiliser pour se connecter (sous la forme CN=AdminGLPI,OU=users,DC=mycompany,DC=local)
- **Mot de passe:** mot de passe associé au compte
- **Champ de l’identifiant:** identifiant LDAP utilisé pour rechercher les objets (ajout ou mises à jour). utilisez samaccountname
- **Commentaire:** Un commentaire sur ce serveur.

- Tester la connexion à l'annuaire LDAP:  
![04](/images/GLPI/GLPI_AD/04.PNG)

#### Importer des nouveaux utilisateurs:  

- Cliquez sur **Liaison annuaire LDAP**:  
![05](/images/GLPI/GLPI_AD/05.PNG)

- Cliquez sur **importation de nouveaux utilisateurs**:  
![06](/images/GLPI/GLPI_AD/06.PNG)

- Cliquez sur **rechercher**:
![07](/images/GLPI/GLPI_AD/07.PNG)

- Importez les utilisateurs souhaités:  
![08](/images/GLPI/GLPI_AD/08.PNG)