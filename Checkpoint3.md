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


![Capture d’écran de l'utilisateur_lionel](https://github.com/user-attachments/assets/6ab9bafa-491f-4600-afaf-810d4e30ae22)

Q.1.1.2 Créer une OU DeactivatedUsers et déplace le compte désactivé de Kelly Rhameur dedans.    

![Capture d’écran de kelly](https://github.com/user-attachments/assets/a29c3525-ee91-4738-aff4-c41235fe0530)  
Q.1.1.3 Modifier le groupe de l'OU dans laquelle était Kelly Rhameur en conséquence.  


