## Concepts Rails

> ## La différence entre un site statique et un site dynamique
- *le site non dynamique*: Sur un site non dynamique, une requête en http est envoyée au serveur qui recherche la page en html et la renvoie côté client. La page est interprétée par le navigateur et est affichée à l’utilisateur. Cependant, le principal problème des sites non dynamiques est qu'ils manquent d’interactivité côté client. 
- *le site dynamique*: les langages serveurs comme le PHP facilitent la conception de gros sites, dans un site dynamique le code html n’existe pas encore et va être généré en fonction de paramètres qu’on lui envoie de façon consciente (par le remplissage d’un formulaire par exemple) ou de façon inconsciente (en cliquant sur un lien..). Le script a été fait pour comprendre ces paramètres , on envoie la demande au serveur et ce dernier génère un fichier html.
Le processus est le suivant: l’utilisateur saisit l'URL une page en HTML => la requête est envoyée sur le serveur => localisation de la page PHP concernée => renvoie vers le préprocesseur => interprétation du code PHP envoyée au navigateur


> ## Le MVC (ou *model view controller*) 
Il s'agit d'une une manière de structurer une application et de gérer l’information. Ce n’est pas un *framework* mais une manière de structurer les applications web
1. *view*: gère la présentation et l'affichage côté client.il est inutil de changer le modèle lorsque l’on change la *view*.
2. *controlleur*: le rôle du controleur est de répondre aux interactions/évènements de l’usager, il gère les décisions. Le contrôleur correspond au serveur. Il va intéragir avec l’utilisateur, réaliser les resquests, et demander au modèle ce dont il a besoin 
3. *browser*: communique avec le contrôleur
4. le *modèle* contient le code relatif à la base de donnée, et se charge de la gestion les données (mais ne les contient pas directement). Le modèle communique avec le contrôleur.

En séparant ces différents éléments la structure devient plus solide et évite de se répéter. 
Le client (Chrome/firefox..) interroge le serveur (via des langages serveurs: PHP, Ruby, Python) et *process* l’information (sans la stocker). 


![MVC process](https://helloacm.com/wp-content/uploads/2017/01/model-view-controller-mvc-explained.jpg)



>## Les *routes*
processus qui va du contrôleur au browser, le route processing redirige vers le bon contrôleur. 
Exemple: onglet contact des sites internet
 
> ## Les Bases de Données
La base de donnée est chargée du stockage de l’information. Le serveur va chercher dans la base de donnée une recherche Google par exemple (MySQL, NOSQL, PostgSQL)puis renvoyer la donnée vers le serveur, puis vers le client en HTML/CSS. Pour générer un fichier la plupart du temps le PHP fonctionne le pair avec la base de données en SQL. 

> ## GET / POST
les requêtes HTTP permettent la communication entre les clients et serveurs.  
- POST: requête qui s’accompagne de l’envoie de données au serveur, donc à un script qui les reçoit en paramètres. Les données ne sont pas cachées et ne sont pas enregistrées dans l’historique. Cette méthode est plus sécurisée que GET
- GET pas d’envoie de données mais demande des données d’une source spécifique. Les données envoyées font parties de l’URL

Le concept de migration
Les relations entre les models des BDD
Les fonctions du CRUD
