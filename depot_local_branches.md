# Depot local et branches


## Que se passe-t-il lorsque vous initialisez un dépôt ? Pourquoi doit-on faire ça ? 

L'initialisation d'un dépôt git crée un dossier (caché) `.git` dans le répertoire de travail. 

Il contient toutes les informations pour recréer le répertoire de travail tel qu'il l'était lors de chacun des commits. 


## Quelle est la différence entre le `working directory` et le dépôt ? Quelle est l'intérêt de cette séparation ?


* `working directory` : c'est le dossier dans lequel on travail, il contient les modifications non commitées et les fichiers non ajoutés à git
* dépôt : c'est là où git stocke les informations pour reconstruire le `working directory`

Le `working directory` correspond au dossier du projet tel qu'il est sur le système de fichier. C'est le dossier dans lequel vous travailliez normalement avant de connaître git.

## Comment peut-on utiliser la zone de `staging` pour être sûr d'avoir un commit par changement logique ?

La zone de `staging` va permettre de ne commiter que les éléments pertinents pour ce commit là. Cela permet de n'ajouter que certains des fichiers modifiés s'ils n'ont pas à être dans le même commit. 

Si la `staging` n'existant pas, cela serait beaucoup plus difficile à faire.

## Quelles sont les situations où les branches sont utiles pour garder un historique organisé ? Comment peuvent-elles aider ? 

Les branches permettent de conserver un ensemble de commit sous la même fonctionnalité. Ainsi avec les branches on peut facilement voir à quelle fonctionnalité appartient quel commit.

## Comment les diagrammes de commit peuvent-ils vous aider à visualiser la structure arborescente ? 

Les diagrammes représentent les liens de parent à enfant entre chacun des noeuds que sont les commits. Cela forme une structure arborescente plus facile à conceptualiser.


## Quel est le résultat de la fusion de deux branches ? Comment le représente-t-on dans le diagramme ? 

* 3 way merge : on a un commit avec 2 parents (le commit à 2 flèches qui en parte pour aller vers les 2 parents)
* fast forward : on ne voit rien, le pointeur de la branche est juste déplacé au bout de l'autre.

## Quels sont les avantages et inconvénients de la méthode de fusion automatique de Git par rapport à le faire manuellement ?

Avantages : 
* souvent géré correctement, en ne provoquant pas de conflits

Inconvéniant :
* peut parfois être compliqué quand il y a des conflits