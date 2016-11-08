Github Intro
================
Hao Ye
November 8, 2016

Where do I begin?
-----------------

For a basic review of Git (the version control system) and Github (the code-hosting platform), take a look at Brian Stock's notes from last week ("2016\_11\_01\_github\_intro").

Basic Github Collaboration (shared repository model)
----------------------------------------------------

1.  You want to start with an up-to-date local copy of the shared repository. If you don't currently have a local copy, you can create one using the `git clone` command. Otherwise, just pull the most recent changes.

2.  Make a new branch for your changes. This allows you to make changes and commit them without worrying that you'll be causing a conflict with someone else's commits. Please choose a descriptive name for the new branch (maybe even including your username).

\[Note that we are running these commands in the shell.\]

        $ git checkout -b hye_github_collab

1.  This should create the new branch and set our local Git repo to point to that branch. We can now make changes, and commit them to this new branch.

2.  Once your changes are committed, you can go back to the `master` branch using the RStudio interface or the shell command.

<!-- -->

        $ git checkout master

1.  Then make sure to pull the latest version of the `master` branch before attempting to merge your new changes.

2.  Now try to merge your changes. (The `--no-ff` option is to make sure all our individual branch commits are not collapsed into a single commit on the `master` branch.)

<!-- -->

        $ git merge --no-ff hye_github_collab

1.  Resolve any conflicts (probably none if you're only adding new files), and go back to 6. to try merging again.

2.  Now push the changes back to Github.

3.  Delete your local copy of the new branch, since its work is now done!

<!-- -->

        $ git branch -d hye_github_collab