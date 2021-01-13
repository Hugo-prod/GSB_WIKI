+++
title = "Installer Active Directory + DNS "
date = "2020-11-16"
+++


- Cliquez sur **Gérer**, puis sur **Ajouter des rôles et fonctionnalités**:  
![01](/images/windows_ad_dns/01.PNG)

---

- **Suivant**:  
![02](/images/windows_ad_dns/02.PNG)

---

- **Installation basée sur un rôle ou une fonctionnalité**:  
![03](/images/windows_ad_dns/03.PNG)

---

- Sélectionner le serveur puis **suivant**:  
![04](/images/windows_ad_dns/04.PNG)

---

- Sélectionner le rôle **AD DS** et **DNS**:  
![05](/images/windows_ad_dns/05.PNG)

---

- **Suivant**:  
![06](/images/windows_ad_dns/06.PNG)

---

- **Suivant**:  
![07](/images/windows_ad_dns/07.PNG)

---

- **Suivant**:
![08](/images/windows_ad_dns/08.PNG)

---

- **Installer**:  
![09](/images/windows_ad_dns/09.PNG)

---  

- L'installation est en cours:  
![10](/images/windows_ad_dns/10.PNG)

---

- Nous pouvons aperçevoir le petit panneau :warning:
- Cliquer dessus, nous devons promouvoir ce serveur en **contrôleur de domaine**:  
![11](/images/windows_ad_dns/11.PNG)

---

- Voici l'assitant de configuration de déploiement:
- **Ajouter une nouvelle forêt**:
- Choissiez un nom pour votre nom de domaine racine:  
![12](/images/windows_ad_dns/12.PNG)

---  

- Saisissez un mot de passe:  
![13](/images/windows_ad_dns/13.PNG)

---  

- **Suivant**:  
![14](/images/windows_ad_dns/14.PNG)

---

- **Suivant**:
![15](/images/windows_ad_dns/15.PNG)

---

- **Suivant**:  
![17](/images/windows_ad_dns/17.PNG)

---

- **Suivant**:  
![18](/images/windows_ad_dns/18.PNG)

---

- Voici le contenu exact des sélections:  
![19](/images/windows_ad_dns/19.PNG)

---

- Voici l'equivalent de la configurations en script **PowerShell**:  
![20](/images/windows_ad_dns/20.PNG)

---

- Procéder à l'installation:  
![21](/images/windows_ad_dns/21.PNG)

---
