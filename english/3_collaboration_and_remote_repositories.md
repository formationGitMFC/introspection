# Remote Repository and Collaboration

## When will you use a remote repository compared to a local repository?

* When there is collaboration (collaboration can be between multiple computers of the same person).
* As a backup system.
    * Note: This does not replace a real backup system.

## Why do you need to pull updates manually to keep the repository synchronized? Why doesn't Git do this automatically?

* Pulling automatically may cause more problems than benefits.
* You need the internet to pull.
* A notification mechanism would be required for Git to know when to pull automatically.

## Explain the difference between a `fork`, a clone, and branches. When would you use each of these concepts?

* Fork: Creates a new project from an existing project. This is a GitHub-specific mechanism and contributes to the popularity of the initial project (tracking statistics).
* Clone: Copies a remote repository locally while retaining a `remote` to the distant URL. This is usually done only once in the project's lifecycle; the rest of the synchronization is done via `push`, `pull` / `fetch`.
* Branch: Allows duplicating the current state of a repository to develop multiple things in parallel. There are several types of branches:
    * Local branches: They are not shared and exist only on the local repository.
    * Remote branches: They are shared and can be used by all project members.

## What is the advantage of having the latest known state of the remote repository stored locally?

It allows knowing the state of the `remote` at any time.
Additionally, it separates the synchronization step (which requires internet) from the merging step (which does not).
Finally, it enables using the same branch-based mechanism whether you have internet access at the time you seek to collaborate or not.

## How would you collaborate without Git or GitHub? Would it be more difficult or simpler?

It depends on the profile and type of collaboration:
* Technical people / text files: I would use Git via the command line with advanced collaboration concepts.
* Less technical people / text files (essentially to replace emails): I would teach them Git with a graphical client.
* Large files / binary files: Git would only serve for synchronization as diffs wouldn't work; I might use something else.

## When is it more advantageous to make changes in a dedicated branch rather than in the master branch? What are the advantages of each approach?

* Changes in master:
    * Risk of deploying something broken or untested.
    * Faster to implement.
* Changes in a branch:
    * Takes longer to set up.
    * Allows review/testing of changes.