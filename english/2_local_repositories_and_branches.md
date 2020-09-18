# Local Repository and Branches

## What happens when you initialize a repository? Why should you do it?

Initializing a git repository creates a (hidden) `.git` folder in the working directory. 

It contains all the information needed to recreate the working directory as it was at the time of each commit.

## What is the difference between the `working directory` and the repository? What is the benefit of this separation?

* `working directory`: It's the folder where you work; it contains uncommitted changes and files not added to git.
* Repository: This is where git stores the information to rebuild the `working directory`.

The `working directory` corresponds to the project folder as it is on the file system. It's the folder you worked in normally before knowing git.

## How can you use the `staging` area to ensure you have one commit per logical change?

The `staging` area allows you to commit only the relevant elements for that specific commit. This allows you to add only certain modified files if they do not need to be in the same commit.

If the `staging` area didn't exist, it would be much more challenging to do this.

## In what situations are branches useful for keeping an organized history? How can they help?

Branches allow you to keep a set of commits under the same functionality. Thus, with branches, you can easily see which commits belong to which functionality.

## How can commit diagrams help you visualize the tree structure?

Diagrams represent the parent-child links between each commit node. This forms a tree structure that is easier to conceptualize.

## What is the result of merging two branches? How is it represented in the diagram?

* 3-way merge: You have a commit with 2 parents (the commit has 2 arrows pointing to the 2 parents).
* Fast forward: Nothing is shown; the branch pointer is just moved to the end of the other.

## What are the advantages and disadvantages of Git's automatic merge method compared to doing it manually?

Advantages:
* Often handled correctly, avoiding conflicts.

Disadvantage:
* Can sometimes be complicated when there are conflicts.