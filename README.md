## Concepts Rails

> ## La différence entre un site statique et un site dynamique
* *le site non dynamique*: Sur un site non dynamique, une requête en http est envoyée au serveur qui recherche la page en html et la renvoie côté client. La page est interprétée par le navigateur et est affichée à l’utilisateur. Cependant, le principal problème des sites non dynamiques est qu'ils manquent d’interactivité côté client. 
* *le site dynamique*: Les sites dynamiques favorisent les interactions avec le client. Ce type de site exécute des programmes capables d'afficher des informations différentes en fonction du besoin et des requêtes. C’est le rôle du serveur web, il exécute la page dynamique (qui peut par exemple afficher la liste de tous les messages d’un utilisateur) et la transforme en HTML afin qu’elle soit affichable par le navigateur internet.
Dans le cas d'une application web, il s'agit de sites dynamiques.

Le processus est le suivant: l’utilisateur saisit l'URL une page en HTML => la requête est envoyée sur le serveur => localisation de la page PHP concernée => renvoie vers le préprocesseur => interprétation du code PHP envoyée au navigateur


> ## Le MVC (ou *model view controller*) 
Il s'agit d'une une manière de structurer une application et de gérer l’information. Ce n’est pas un *framework* mais une manière de structurer les applications web
1. *la vue*: gère la présentation et l'affichage côté client, en d'autres termes la vue traite ce que l'on voit à l'écran. Il est inutile de changer le modèle lorsque l’on change de vue.
2. *contrôleur*: le rôle du controleur est de répondre aux interactions/évènements de l’usager, il gère les décisions. Le contrôleur correspond au serveur. Il va intéragir avec l’utilisateur, réaliser les resquests, et demander au modèle ce dont il a besoin. En somme, pour une action donnée de l'utilisateur, il va déterminer quels traitements doivent être effectués. Il interprète la requête HTTP entrante et choisit la vue à afficher dans le navigateur.
3. *browser*: communique avec le contrôleur
4. le *modèle* contient le code relatif à la base de donnée, et se charge de la gestion les données (mais ne les contient pas directement). Le modèle communique avec le contrôleur.Il s’agit en général d'un ensemble de classes permettant d’accéder à vos données.

En séparant ces différents éléments la structure devient plus solide et évite de se répéter. 
Le client (Chrome/firefox..) interroge le serveur (via des langages serveurs: PHP, Ruby, Python) et *process* l’information (sans la stocker). 

![MVC_explained](https://raw.githubusercontent.com/mdang/resources/master/ruby/rails/rails_architecture.png)


>## Les *routes*
Le routes permet de transformer une URL en une action du contrôleur. Aiguille les requêtes des utilisateurs vers l'application. Cela permet de réagir différemment en fonction de ce que souhaite faire l'utilisateur
 
> ## Les Bases de Données
La base de donnée est chargée du stockage de l’information. Le serveur va chercher dans la base de donnée une recherche Google par exemple (MySQL, NOSQL, PostgSQL)puis renvoyer la donnée vers le serveur, puis vers le client en HTML/CSS. Pour générer un fichier la plupart du temps le PHP fonctionne le pair avec la base de données en SQL. 

> ## GET / POST
les requêtes HTTP permettent la communication entre les clients et serveurs.  
- *POST*: requête qui s’accompagne de l’envoie de données au serveur, donc à un script qui les reçoit en paramètres. Cette méthode est plus sécurisée que GET, cette requête ne doit pas pouvoir être réexécutée et modifie les données.
Exemple: formulaire HTML d'un site web pour réaliser son inscription
- *GET* permet d'obtenir une ressource du site web en lecture seule, demande des données d’une source spécifique (demande au serveur web par exemple d'afficher une page en HTML). Les données envoyées font parties de l’URL, elles sont passées en paramètres à la requête GET. Il est possible de passer plusieurs paramètres à une requête GET, il suffit d’enchaîner les paramètres et de les séparer par le symbole &. 
Exemple:  http://fr.openclassrooms.com/pagedecours.html?cours=ASP.NET&auteur=nico.pyright
La requete GET doit pouvoir etre exécutée à l'infinie et ne doit pas modifier le contenu d'une page. 

> ## Le concept de migration
Transition de l'ancien système informatique au nouveau. Le point le plus important de la migration des systèmes informatiques est la migration des données. Les migrations peuvent être réalisées au niveau technique (automatiquement) ou organisationnel (manuellement). 
Le concept de migration prend en compte les quantités, les fréquences et la qualité des données dans l’ancien système ainsi que leur intégration dans le nouveau. Les scénarios de migration possibles sont analysés et évalués, de manière que l’on puisse déterminer les procédures appropriées.
Les réflexions sur la migration portent sur sa faisabilité, son efficience, sa qualité et son déroulement dans le temps.
Avec la migration des données se posent aussi des questions d’archivage des anciennes données et de démantèlement du système, auxquelles il faut répondre. Les aspects relatifs à la sécurité et à la protection des données doivent être pris en compte.


> ## Les relations entre les models des BDD
Des relations de différents types peuvent exister entre les bases de données. Elles sont définies par: 
* leur cardinalité

> ## Les fonctions du CRUD
Il s'agit d'un système de manipulation de base de données, cet acronyme indique les 4 opérations de base pour gérer tous types de données.
Les fonctions sont :

Create (ou création),
Read (ou lecture),
Update (modification),
Delete (Suppression).
