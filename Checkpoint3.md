# Exercice 2 : Manipulations pratiques sur VM Linux
## Partie 1 : Gestion des utilisateurs
Q.2.1.1 Sur le serveur, créer un compte pour ton usage personnel.  
![création_utilisateur](https://github.com/user-attachments/assets/6fcd56a4-964b-4e4e-9def-420ab903b53e)    
Q.2.1.2 Quelles préconisations proposes-tu concernant ce compte ?  
Renommer le compte s’il s’agit du compte administrateur par défaut.  

Définir un mot de passe fort et sécurisé.  

Forcer le changement de mot de passe à la première connexion.  

Désactiver ou supprimer les comptes inutilisés ou temporaires.   

Surveiller l’activité du compte via les journaux système.  

Ne pas utiliser le compte admin pour un usage courant.  

# Partie 2 : Configuration de SSH
Q.2.2.1 Désactiver complètement l'accès à distance de l'utilisateur root.      
![Capture d’écran désactivation_d'utisateur-root1](https://github.com/user-attachments/assets/eb31d3b1-3288-4e16-9b38-e73172877872)    

# Partie 3 : Analyse du stockage  
Q.2.3.1 Quels sont les systèmes de fichiers actuellement montés ?    
![Capture d’écran du fichier_montés](https://github.com/user-attachments/assets/db820aa2-4c89-4d19-b81f-77c6289ad914)  
Q.2.3.2 Quel type de système de stockage ils utilisent ?  
il utilise le stokage SDD  
Q.2.3.3 Ajouter un nouveau disque de 8,00 Gio au serveur et réparer le volume RAID   
![Capture d’écran du RAID](https://github.com/user-attachments/assets/139653db-df74-4dab-8283-d999baf6d491)    

Q.2.3.5 Combien d'espace disponible reste-t-il dans le groupe de volume ?  
![Capture d’écran du d'espace_restant](https://github.com/user-attachments/assets/52249378-2451-4d46-b6f4-5c9f4a95b32e)    
# Partie 4 : Sauvegardes  
Q.2.4.1 Expliquer succinctement les rôles respectifs des 3 composants bareos installés sur la VM.    
bareos-dir : contrôle et planifie les sauvegardes  

bareos-fd : envoie les fichiers à sauvegarder  

bareos-sd : stocke les fichiers reçus  

# Partie 5 : Filtrage et analyse réseau  

Q.2.5.1 Quelles sont actuellement les règles appliquées sur Netfilter ?   
Netfilter est le système de filtrage réseau utilisé par Linux pour appliquer des règles de pare-feu.  
Q.2.5.2 Quels types de communications sont autorisées ?  

Les communications autorisées sont :  
SSH ,HTTP,HTTPS, DNS , DHCP ,ICMP    
Q.2.5.3 Quels types sont interdit ?  
Accès root SSH  
Ports non utilisés ou non sécurisés    
Trafic ICMP non essentiel    
Q.2.5.4 Sur nftables, ajouter les règles nécessaires pour autoriser bareos à communiquer avec les clients bareos potentiellement présents sur l'ensemble des machines du réseau local sur lequel se trouve le serveur.  
Pour autoriser Bareos à communiquer avec ses clients sur le réseau local via nftables, il faut ouvrir les ports utilisés par Bareos. Par défaut, Bareos utilise :  

    - Port 9101 TCP : bareos-dir    

   - Port 9102 TCP : bareos-fd    

   - Port 9103 TCP : bareos-sd   
# Exercice 1 : Manipulations pratiques sur VM Windows # 
Q.1.1.1 Créer l'utilisateur Lionel Lemarchand avec les même attribut de société que Kelly Rhameur.  
![Capture d’écran de la création de l'utilisateur lionel](https://github.com/user-attachments/assets/d0dcec85-53ab-47e0-ad29-4206ea11f7f6)

![Capture d’écran de la suite](https://github.com/user-attachments/assets/11db54d6-ade9-4cb8-b066-c7b55017f5d1)



Q.1.1.2 Créer une OU DeactivatedUsers et déplace le compte désactivé de Kelly Rhameur dedans.    

Trouve l’utilisateur Kelly Rhameur  

Clique droit sur son nom → Désactiver le compte   
 Déplacer Kelly vers "DeactivatedUsers"  

 Clique droit sur Kelly Rhameur → Déplacer  

Sélectionne l’OU DeactivatedUsers  

 Clique sur OK  
 ![Capture d’écran de la deactivation de Kelly Rhameur](https://github.com/user-attachments/assets/31c31ca5-7b6e-4af1-9ca7-04ccbca02fe9)


Q.1.1.3 Modifier le groupe de l'OU dans laquelle était Kelly Rhameur en conséquence.    

![Capture d’écran de la modification de OU](https://github.com/user-attachments/assets/6bc50011-4345-49d4-a85d-c42a18b06d27)  


![Capture d’écran suite](https://github.com/user-attachments/assets/e7cb8e42-3c84-4d94-ae19-4f96e9c38d04)  

# Partie 2 : Restriction utilisateurs  

Q.1.2.1 Faire en sorte que l'utilisateur Gabriel Ghul ne puisse se connecter que du lundi au vendredi, de 7h à 17h.  
![Capture d’écran du temps de connexion de Gabriel](https://github.com/user-attachments/assets/d96a4e77-146a-4ba3-8b76-a917cc03cfec)  

Q.1.2.2 De même, bloquer sa connexion au seul ordinateur CLIENT01.  

![Capture d’écran de la connexion du client01](https://github.com/user-attachments/assets/64c1796e-bfd3-442a-8e7a-5f8f135b0dda)  


![Capture d’écran suit](https://github.com/user-attachments/assets/5153422d-6c20-48f2-85e2-caa18cc37c38)  

Q.1.2.3 Mettre en place une stratégie de mot de passe pour durcir les comptes des utilisateurs de l'OU LabUsers.  

# Partie 3 : Lecteurs réseaux  
Q.1.3.1 Créer une GPO Drive-Mount qui monte les lecteurs E: et F: sur les clients.  



