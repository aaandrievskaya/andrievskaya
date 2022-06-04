---
title: Управление версиями. Гит
subtitle: Изучим идеологию и применение инструментов контроля версий. Овладейте навыками работы с git.

# Summary for listings and search engines
summary: Изучим идеологию и применение инструментов контроля версий. Овладейте навыками работы с git.
# Link this post to the project
projects: []

# Date published
date: '2022-05-07'


# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false


authors:
  - администратор
  - Андриевская А.А.

tags:
  - Работа
  - Git

categories:
  - Demo
---

## Version control systems. General concepts

Version control systems (VCS) are used when several people work on the same project. Usually the main project tree is stored in the local
or a remote repository to which access is configured for project members. At
making changes to the content of the project, the version control system allows them to
fix, combine changes made by different project participants,
rollback to any earlier version of the project, if required.
Classical version control systems use a centralized model,
assuming a single repository for storing files. Most of the version control functions are performed by a dedicated server.
The project participant (user) before starting work through certain
command gets the version of files it needs. After making changes, the user
commits the new version to the repository. This does not remove previous versions.
from the central repository and you can return to them at any time. The server can
save not the full version of the changed files, but produce the so-called delta compression - save only changes between successive versions, which
allows you to reduce the amount of stored data.
Version control systems support traceability and resolution
conflicts that may arise when several people work on one
file. You can merge (merge) the changes made by different participants (automatically or manually), manually select the desired version, undo the changes altogether
or lock files for modification. Depending on the settings, blocking is not
allows other users to get a working copy or prevents modification
working copy of the file by means of the OS file system, thus providing
privileged access to only one user working with the file.
Version control systems can also provide additional, more flexible
functionality. For example, they can support working with multiple versions of the same file, keeping a common history of changes up to the branch point.
versions and each branch's own change histories. In addition, it is usually available
information about which of the participants, when and what changes were made. Usually this
kind of information is stored in the change log, access to which can be restricted.
Unlike classical ones, in distributed version control systems, the central
the repository is optional.
Among the classic VCS, CVS, Subversion are the most famous, and among the distributed ones - Git, Bazaar, Mercurial. The principles of their work are similar, they differ mainly
the syntax of the commands used in the work.

## Basic git commands

The most commonly used git commands are:
– creating the main repository tree:

1 git init

– receiving updates (changes) of the current tree from the central repository:

1 git pull

– sending all the changes made to the local tree to the central repository:

1 git push

– view the list of changed files in the current directory:

1 git status

– view current changes:

1 git diff

– saving current changes:
– add all modified and/or created files and/or directories:

1 git add .

– add specific modified and/or created files and/or directories:

1 git add filenames

– delete a file and/or directory from the repository index (in this case, the file and/or directory
remains in the local directory):

1 git rm filenames

– saving the added changes:
– save all added changes and all modified files:

1 git commit -am 'Commit description'

- save the added changes with a comment through the built-in
editor:

1 git commit

– creating a new branch based on the current one:

1 git checkout -b branchname

- switch to some branch:

1 git checkout branch_name

(when you switch to a branch that is not yet in the local repository, it will be
created and linked to the remote)
– pushing changes of a specific branch to the central repository:

1 git push origin branchname

– merge the branch with the current tree:

1 git merge --no-ff branchname

- deleting a branch:
– deleting a local branch already merged with the main tree:

1 git branch -d branchname

- forced deletion of the local branch:

1 git branch -D branchname

– deleting a branch from the central repository:

1 git push origin :branchname

## Standard Operating Procedures for a Central Repository

The work of the user with his branch begins with checking and receiving changes
from the central repository (at the same time, to the local tree before starting this procedure
should not be changed):

1 git checkout master
2 git-pull
3 git checkout -b branchname

You can then make changes in the local tree and/or branch.
After the completion of making some change to the files and / or directories of the project
you need to place them in the central repository. To do this, you need to check,
which files have changed so far:

1 git status

and, if necessary, delete unnecessary files that we do not want to send to the central repository.
Then it is useful to review the text of the changes for compliance with the rules for maintaining clean commits:

1 git diff

If some files should not be included in the commit, then we mark only those files that
whose changes you want to save. To do this, use the commands add and/or
deletion with the necessary options:

1 git add ...
2 git rm ...

If you want to save all changes in the current directory, then use:

1 git add .

Then we save the changes, explaining what was done:

1 git commit -am "Some commit message"

and send it to the central repository:

1 git push origin branchname
or
1 git push

## Working with a local repository
Let's create a local repository.
First, let's make a preliminary configuration by specifying the name and email of the owner of the repository:

1 git config --global user.name "FirstName LastName"
2 git config --global user.email "work@mail"

and setting utf-8 in git output:

1 git config --global quotepath false

To initialize a local repository located, for example, in a directory
~/tutorial must be typed on the command line:

1 cd
2 mkdir tutorial
3 cd tutorial
4 git init

After that, a .git directory will appear in the tutorial directory, in which it will be stored
change history.
Let's create a test text file hello.txt and add it to the local repository:

1 echo 'hello world' > hello.txt
2 git add hello.txt
3 git commit -am 'New file'

Let's use the status command to view the changes in the working directory since the last revision:

1 git status

While working on a project, one way or another, files can be created that are not
needs to be added to the repository later. For example, temporary files created by editors or object files created by compilers. Can prescribe templates of file types ignored when adding to the repository in the file .gitignore with services. To do this, you first need to get a list of available
templates:

curl -L -s https://www.gitignore.io/api/list

Then download the template, for example, for C and C++

curl -L -s https://www.gitignore.io/api/c >> .gitignore
curl -L -s https://www.gitignore.io/api/c++ >> .gitignore

## Working with the repository server
For subsequent user identification on the repository server, it is necessary
generate a key pair (private and public):

1 ssh-keygen -C "First Name Last Name <work@mail>"

The keys are stored in the ~/.ssh/ directory.
There are several repository servers available with the option of free
data placement. For example, https://github.com/.
To work with it, you must first create an account on the website https://github.com/. Then you need to upload the public key we generated earlier. For
To do this, go to https://github.com/ under your account and go to the GitHub setting menu. After that, select SSH keys in the GitHub setting side menu and click
the Add Key button. By copying the key from the local console to the clipboard

1 cat ~/.ssh/id_rsa.pub | xclip -sel clip

paste the key into the field that appears on the site.
After that, you can create a repository on the site by selecting Repositories from the menu
Create a repository, give it a name and make it public (public).
To download the repository from the local directory to the server, execute the following
commands:

1 git remote add origin
2 ssh://git@github.com/<username>/<reponame>.git
3 git push -u origin master

Further, on the local computer, you can perform standard procedures for working
with git if there is a central repository.

## General information

– Gitflow Workflow published and popularized by Vincent Driessen of Gitflow
vie.
– Gitflow Workflow involves building a strict branching model, taking into account
project release.
– This model is great for organizing a release-based workflow.
– Working on the Gitflow model includes creating a separate branch for bug fixes
in the working environment.
– The sequence of actions when working on the Gitflow model:
– The develop branch is created from the master branch.
– A release branch is created from the develop branch.
– Feature branches are created from the develop branch.
– When work on the feature branch is completed, it is merged into the develop branch.
– When work on a release branch is completed, it is merged into branches
develop and master.
– If a problem is found in master, a hotfix branch is created from master.
– When a hotfix branch is completed, it is merged into branches
develop and master.

## Software installation

– For Windows, the Chocolatey package manager is used. Git-flow is included
git package.

1 choco install git

– For MacOS, use the Homebrew package manager.

1 brew install git-flow

– Linux
– Gentoo

1 emerge dev-vcs/git-flow

– Ubuntu

1 apt-get install git-flow

## Work process with Gitflow

### Main branches (master) and development branches (develop)

To commit the history of the project within this process instead of a single master branch
two branches are used. The master branch holds the official release history, while the develop branch is for merging all the features. In addition, for convenience
it is recommended to give all commits in the master branch a version number.
When using the git-flow extension library, you need to initialize the structure in an existing repository:

1 git flow init

For github, the Version tag prefix should be set to v.
After that, check which branch you are on:

1 git branch

### Feature branches

Each new feature should have its own branch, which can be
send to the central repository for backup or sharing
team work. Feature branches are created not on the basis of master, but on the basis of develop.
When work on a feature is completed, the corresponding branch is merged back
with the develop branch. Features should not be pushed directly to the master branch.
Typically, feature branches are created from the latest develop branch.

### Creating a feature branch

Let's create a new feature branch:

1 git flow feature start feature_branch

Further we work as usual

### End of work on a feature branch

Upon completion of work on a feature
merge feature_branch with develop:

1 git flow feature finish feature_branch

### Release branches

When the develop branch has enough features to release, the develop branch
a release branch is created. Creating this branch starts the next release cycle,
and from that moment on, new functions can no longer be added - only debugging is allowed,
creating documentation and solving other problems. When the release preparation is completed,
the release branch is merged into master and given a version number. After that, you need to merge with the develop branch, in which, since the creation of the release branch,
changes occur.
Due to the fact that a special branch is used for preparing releases, one
a team can refine the current release while another team continues
work on features for the next one.
You can create a new release branch with the following command:

1 git flow release start 1.0.0

The following commands are used to complete work on the release branch:

1 git flow release finish 1.0.0

### Hotfix branches

Support branches or hotfix branches are used for quick fixes
to working releases. They are created from the master branch. This is the only thread that
must be created directly from master. Once the fix is ​​complete,
the branch should be merged into master and develop. The master branch should be tagged with an updated version number.
Having a dedicated branch for fixing bugs allows the team to resolve issues without interrupting the rest of the workflow or waiting for the next cycle.
release.
A hotfix branch can be created with the following commands:

1 git flow hotfix start hotfix_branch

When finished, the hotfix branch is merged into master and develop:

1 git flow hotfix finish hotfix_branch


