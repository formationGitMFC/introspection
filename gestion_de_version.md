# Concept de gestion de version

## En quoi accéder au diff entre deux version d'un fichier peut vous aider à trouver des bugs ? 

Avoir la différence entre les fichiers permet de savoir les évolutions du code :

* elles sont listées, il n'y a pas besoin de s'en rappeler
* on peut voir si les différences sont effectivement celles que l'on imaginait avoir codé

Si le code fonctionnait avant, on peut voir où la régression a eu lieu. 


## En quoi l'accès facile à l'historique des fichiers peut vous aider à devenir meilleurs développeurs ? 

On peut voir la progression du code. 


## Quels sont, selon vous, les avantages et inconvénients que l'on peut avoir à choisir manuellement les fichiers commités et quand, comme il est d'usage dans git, par rapport à un système automatisé google Google doc ?

* Avantages :
    * les commits ont une consistance logique (un commit == un set d'actions bien défini)
    * si l'on modifie plusieurs fichiers sans les commiter, on peut n'en sélectionner qu'une partie pour le commit à venir


* Inconvénients :
    * il ne faut pas oublier de faire les commits, si vous n'en faites pas, ils ne se feront pas 


## Pourquoi, selon vous, Git permet d'intégrer plusieurs fichiers à un commit alors que pour les Google Doc, les fichiers sont gérés séparément ?

Les fichiers de code ont souvent des dépendances entre eux (modules et codes les appelants, fichiers .c / .h, fichiers CSS et HTML...)


## Comment utiliser les commandes `git log` et `git diff` pour visualiser l'historique d'un fichier ?

* `git log --follow -p -- [filename]` : affiche les commits touchant le fichier avec les diff (option `-p`) et le suivi de renommage 
* `gitk [filename]` : permet de visualiser les modifications apportés à un fichier précis
* `git diff [filename]`: affiche le diff d'un fichier 


## En quoi utiliser un système de gestion de version peut vous aider à être plus confiant dans votre capacité à ne rien casser dans le code ?

* On peut revenir en arrière facilement 
* On peut avoir les différentes versions (fonctionnelle et modification) en parallèle avec les branches
* On peut vérifier que les modifications ne touchent qu'un ensemble de lignes précises (en pratique, le code est complexe, une petite modification peut avoir de grosses répercussions)

## Maintenant que vous avez configuré git, comment allez-vous l'utiliser au jour le jour ? 

Oui. Je l'utilise déjà pour mes projets pros comme système de partage de code et de sauvegarde. 

Je l'utilise également sur mes projets personnels. 