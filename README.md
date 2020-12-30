# Design-Pattern-Command

Description du design pattern Command
[la vidéo](https://youtu.be/z6NOc4TXZDo)

***
## Préambule 

Lors du module M3105, intitulé Conception & Programmation orienté objet, j’ai appris les bonnes pratiques, les doublures de test, les principes SOLID et les Design Patterns. Dans ce cadre, j’ai réalisé une présentation sur un design pattern de mon choix et choisi de présenter le design pattern Command. Pour faciliter la compréhension nous avons réalisé une vidéo. 

***
## Contenu

***

### Qu’est-ce qu’un Design Pattern ? 

Les design patterns ont été formalisés pour la première fois par le « Gang of Four » dans un livre intitulé Design Patterns – Elements of Reusable Object-Oriented Software paru en 1994.
En informatique, et plus particulièrement en développement logiciel, un design pattern est un arrangement caractéristique de modules. Un pattern va permettre de résoudre un problème grâce à un modèle de résolution. 

**Il existe 3 types de Design Pattern :** 
-	Le design pattern Création
-	Le design pattern Structure
-	Le design pattern Comportemental

***

### Le pattern Command 

Pattern de type **comportemental**, c’est-à-dire qu’il permet d’augmenter la souplesse dans l’exécution de cette communication.

*L’intention du design pattern **Command*** est de transformer une requête en un objet, facilitant ainsi des opérations comme l’annulation, la mise en file des requêtes et leur suivi.


*Une métaphore est **la commande au restaurant**.*

Un serveur prend une commande en salle, il l’écrit sur un bout de papier. Il se rend dans la cuisine et colle la commande sur le mur. Au bout d’un moment, le chef arrive à la commande, il l’a lie et prépare le plat. Le cuisinier place le repas sur un plateau avec la commande. Le serveur découvre le plateau, vérifie la commande pour s’assure que tout est conforme et l’apporte en salle.

Le bout de papier joue le rôle de la commande. Il reste dans une file d’attente jusqu’à ce que le chef soit prêt à la servir. Le client du restaurant représente la classe Client, qui attend que l’action qu’il a demandée se fasse. Le serveur représente Invoker, qui va placer la commande dans la file d’attente pour qu’elle soit réalisée. Le Receiver est le cuisinier, qui va lire la commande et réaliser l’action correspondante.
Image diagramme

**Diagramme de classe générique du pattern Command**
 
 <img src="https://zupimages.net/up/20/53/up5i.png">

*Les classes participantes à ce patron sont les suivantes :*

**Command** --> fournit une interface qui encapsule une opération pour l'exécuter en différé.
**ConcreteCommand** --> Celle-ci implémente l’interface Command et définit une liaison entre un objet récepteur et une action, et concrétise la méthode execute () pour l'invocation des opérations du récepteur. C’est quoi execute () ? C’est la méthode qui appelle simplement l'action sur le récepteur. 
**Client** --> Cette classe crée un objet ConcreteCommand et positionne son récepteur.
Une autre classe est la classe Invoker. Elle demande à la classe Command d'exécuter sa requête.
**Receive** --> c’est l'objet (ou un des objets) sur lequel s'applique la commande, c’est le récepteur.

**Diagramme de séquence**

<img src="https://zupimages.net/up/20/53/tsw4.png">








