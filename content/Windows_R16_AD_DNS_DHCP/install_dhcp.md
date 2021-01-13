+++
title = "Installer DHCP"
author = "Hugo Grosot"
date = "2020-11-10"
+++


- Cliquez sur **Gérer**, puis sur **Ajouter des rôles et fonctionnalités**:  
![01](/images/windows_dhcp/01.PNG)

---  

- **Suivant**:
![02](/images/windows_dhcp/02.PNG)

---

- Sélectionner le type d’installation **Installation basée sur un rôle ou une fonctionnalité**:
![03](/images/windows_dhcp/03.PNG)

---

- Selectionner le serveur puis **suivant**:
![04](/images/windows_dhcp/04.PNG)

---

- Sélectionner le rôle **Serveur DHCP**:
![05](/images/windows_dhcp/05.PNG)

---

- Valider avec **Suivant**:
![06](/images/windows_dhcp/06.PNG)

---

- Ici vous pouvez constater toutes les fonctionnalités disponnible, dans notre cas nous n'en avons besoin d'aucune, cliquez sur **Suivant**:
![07](/images/windows_dhcp/07.PNG)

---

- :warning: Rappel: votre serveur doit avoir une **IP fixée** ! :warning:  
- Cliquez sur **suivant**: 
![08](/images/windows_dhcp/08.PNG)

---

- Vous pouvez maintenant **l'installer**:
![09](/images/windows_dhcp/09.PNG)

---

- Patienter pendant l'installation:
![10](/images/windows_dhcp/10.PNG)

---

- L'installation est maintenant finit, cliquez sur **Fermer**:
![11](/images/windows_dhcp/11.PNG)

---

On peut maintenant aperçevoir un petit drapeau avec un :warning: car le serveur **DHCP** nécessite encore quelques manipulations
- Cliquez **Terminer la configuration DHCP**:
![12](/images/windows_dhcp/12.PNG)

---

- **Valider**:
![13](/images/windows_dhcp/13.PNG)

---

- **Fermer**:
![14](/images/windows_dhcp/14.PNG)

---

Maintenant que le serveur DHCP est installé, il nous reste plus qu'à le configurer, pour ce faire
- Ouvrez le pannel de configuration du serveur DHCP, depuis le menu **Outils**, puis sélectionnez **DHCP**:
![16](/images/windows_dhcp/16.PNG)

---

Nous allons créer une **Nouvelle étendue** qui aura pour effet de paramétrer une plage d'adresse IP disponible aux clients 
- Clique droit sur **IPv4**
- Clique gauche **Nouvelle étendue**  
![17](/images/windows_dhcp/17.PNG)

---

- **Suivant**:  
![18](/images/windows_dhcp/18.PNG)

---

- Nommez la nouvelle étendu:  
![19](/images/windows_dhcp/19.PNG)

---

- Saisissez une plage d'adresse IP:  
![20](/images/windows_dhcp/20.PNG)

---

- Vous pouvez sélectionner des adresses IP à exclure et même attribuer un retard pour transmettre un message **DHCPOFFER**:  
![21](/images/windows_dhcp/21.PNG)

---

- Voici la durée du bail, vous pouvez également le modifier:  
![22](/images/windows_dhcp/22.PNG)

---

- Sélectionner **Oui** dans le cas où vous avez une **passerelle par défaut** et/ou un **DNS**:  
![23](/images/windows_dhcp/23.PNG)

---

- Saisir votre **Passerelle par défaut**:  
![24](/images/windows_dhcp/24.PNG)

---

- Saisir votre **DNS**:  
![25](/images/windows_dhcp/25.PNG)

---

- Activer l'étendue:  
![27](/images/windows_dhcp/27.PNG)

---

- Terminer:  
![28](/images/windows_dhcp/28.PNG)

---

- Nous pouvons constater que l'étendue a bien été créée:  
![29](/images/windows_dhcp/29.PNG)

---

- On peut consulter les baux attribués:
![30](/images/windows_dhcp/30.PNG)

---