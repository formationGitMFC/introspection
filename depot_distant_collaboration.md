# Depot distant et collaboration


## Quand allez-vous utiliser un dépôt distant par rapport à un dépôt local ?  

* lorsqu'il y a une collaboration (la collaboration peut-être entre plusieurs ordinateurs de la même personne) 
* comme système de sauvegarde
    * attention cela ne remplace pas un réel système de sauvegardes

## Pourquoi devez-vous tirer les modifications à la main pour garder le dépôt synchronisé, pourquoi git ne le fait-il pas automatiquement ? 

* puller automatiquement risque de provoquer plus de problèmes que d'avantages 
* il y a besoin d'internet pour puller
* il faudrait mettre en place un mécanisme de notifications pour que git sache quand puller automatiquement


## Expliquez la différence entre un `fork`, un clone et les branches. A quelle occasion allez-vous utiliser chacun de ces concepts ? 

* fork : créer un nouveau projet à partir d'un projet existant. C'est un mécanisme propre à Github et cela participe à la popularité du projet initial (comptabilisation de statistiques)
* clone : on va copier un dépôt distant en local, tout en conservant une `remote` vers l'url distante. Cela ne se fait qu'une fois pour toute dans le cycle de vie du projet normalement, le reste de la synchronisation passe par des `push`, `pull` / `fetch`
* branche : permet de dupliquer l'état actuel d'un dépôt pour développer plusieurs choses en parallèle. Il existe plusieurs types de branches 
    * les locales : elles ne sont pas partagées, elles sont uniquement sur le dépôt local
    * les distantes : elles sont partagées et peuvent être utilisées par tous les membres du projet


## Quel est l'avantage de posséder la copie du dernier état connu du dépôt distant stocké localement ? 

Cela permet de connaître l'état de la `remote` à tout instant. 
De plus cela permet de séparer l'étape de synchronisation (où l'on a besoin d'internet) et de celle où l'on effectue les fusions (où l'on en a pas besoin). 

Enfin, cela permet d'avoir le même mécanisme basé sur des branches, que l'on ait internet ou pas au moment om l'on cherche à collaborer. 


## Comment collaboreriez-vous sans git ou github ? Cela serait-il plus difficile ou plus simple ?

Cela dépend du profil et du type de collaboration : 
* personnes techniques / fichiers textes : j'utiliserai git en ligne de commande avec les concepts avancés de collaboration 
* personnes peu techniques / fichiers textes (en gros pour remplacer des emails) : je leur apprendrai git avec un client graphique
* gros fichiers / fichiers binaires : git ne servirait qu'à la synchronisation, les diffs ne marcherait pas, j'utiliserai peut-ête autre chose


## Quand est-il plus avantageux d'effectuer des changements dans une branche dédiée plutôt que dans la branche master ? Quel sont les avantages de chaque approches ? 

* modifications dans master : 
    * risque de mettre en production quelque chose de cassé, qui n'a pas été testé / relu
    * plus rapide à mettre en place 
* modifications dans une branche :
    * plus longs à mettre en place 
    * permet la relecture / test des modifications 