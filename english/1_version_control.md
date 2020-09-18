# Version Control Concept

## How can accessing the diff between two versions of a file help you find bugs?

Having the difference between files allows you to understand the code's evolution:

* They are listed; you don't need to remember everything.
* You can see if the differences match what you thought you had coded.

If the code worked before, you can see where the regression occurred.

## How can easy access to file history help you become better developers?

You can see the progress of the code.

## What are, according to you, the advantages and disadvantages of manually selecting files to commit and when, as is customary in Git, compared to an automated system like Google Docs?

* Advantages:
    * Commits have logical consistency (one commit == one well-defined set of actions).
    * If you modify multiple files without committing them, you can select only a portion for the upcoming commit.

* Disadvantages:
    * You must not forget to make commits; if you don't, they won't be made.

## Why do you think Git allows for multiple files to be included in a commit, while Google Docs manages files separately?

Code files often have dependencies between each other (modules and calling code, .c /.h files, CSS and HTML files...).

## How to use the `git log` and `git diff` commands to view the history of a file?

* `git log --follow -p -- [filename]`: shows commits affecting the file with diffs (option `-p`) and tracks renaming.
* `gitk [filename]`: allows you to visualize changes made to a specific file.
* `git diff [filename]`: shows the diff of a file.

## How can using a version control system help you be more confident in your ability not to break the code?

* You can easily roll back.
* You can have different versions (functional and modified) in parallel with branches.
* You can ensure changes only touch a specific set of lines (in practice, code is complex, a small change can have significant repercussions).

## Now that you have set up Git, how will you use it day-to-day?

Yes. I already use it for my professional projects as a code sharing and backup system.

I also use it for my personal projects.