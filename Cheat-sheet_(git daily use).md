# Git-Github Cheatsheet

🧑‍💻Author : Rithwik_Ramakrishnan

### Basic Setup 

 command | use
 ------- | ------
 ``` git config --global user.name "your name" ``` | set your git user-name
 ``` git config --global user.email "your.email@example.com" ``` | set your git email
 ``` git config --list ``` | list all Git configurations

 ### Initializing & Cloning

command | use
 ------- | ------
``` git init``` | initialize a new git repo in your project
 ```git clone <repo-url>``` | clone or downloading an existing repo

 ### Status & log

command | use
 ------- | ------
 ``` git status ``` | show the current status of changes in working directory
 ``` git log ``` | view commit history
 ``` git log --oneline``` | show shorter commit history

command | use
 ------- | ------
``` git reflog ``` | view history of all changes(even uncommited)
``` git reflog show <branch-name> ``` | show reflog for a specific branch
``` git show <commit-id> ``` | show detailed info for a specific commit

### Working with changes

command | use
 ------- | ------
```git add <file>``` | stage a specific file for commit
```git add . ```| stage all changes in the current dir.
``` git commit -m "message" ``` | commit changes with a message
``` git commit --amend ``` | edit the last commit message or add changes in to it.
``` git commit --amend --no-edit ``` | commit changes without editing.

#### Handling merge conflicts 

``` git diff ``` : compare working directory changes

``` git diff <branch1> <branch2> ``` : compare 2 branches

> To Resolve the conflicts : Open files --> fix conflicts --> then add and commit

***

### Branching & Merging

``` git branch <branch-name>``` : create new branch

``` git checkout <branch-name>``` : switch to a specific branch

```git checkout -b <branch-name>``` : create and switch into a new-branch

``` git branch -d <branch-name>``` : delete local branch (use -D to force delete)

``` git push origin --delete <branch-name>``` : delete remote branch

```git branch ``` : to check local branch

```git branch -a``` : to check local and remote branches.

***

``` git merge <branch-name>``` : merge specific branch innto the current branch


```git rebase <branch-name>``` : Re-apply commits on top of another base

``` git rebase -i head~<n> ``` : Interactive rebase to edit commit history, re-arrange and modify commits(squash,drop,edit)

***

#### Undoing the changes :

```git reset <file>``` : unstage file

reset | command | use-case
----|------|--------
soft | `` git reset --soft head~1 `` | undo last commit, but keep chages staged
hard | `` git reset --hard head~1`` | completely remove last commit
mixed | ```git reset --mixed head~1 or git reset head~1 ``` | undo last commit , keep changes in the working directory (unstaged)


``git revert <commit-id>`` : create a new commit that undoes the specific commit
***

#### Reviewing chnages :

```git show <file> ``` : display changes made to specific file

```git diff <commit-id1> <commit-id2>``` : compare changes between 2 commits

***

#### Stash changes :

``` git stash``` : temporarly save changes

```git stash apply``` : reapply stashed changes without removing them

``` git stash --abort``` : to abort the changes.

``git stash clear`` : remove all stashed entries

```git stash list``` : view stashed changes

***

#### Remote Repo :

``` git remote -v``` : list the remote repo urls

```git remote add origin <url>``` : link your local repo to a remote repo.

```git pull origin <branch-name>``` : pull changes from the remote branch

```git fetch``` : download updates from ther remote with-out merging

```git fetch <remote>``` : fetch updates from a remote

***

### git advanced options :

```git cherry-pick <commit-id> ``` : apply a specific commit from another branch

```git cherry-pick <start-commit-id> <end-commit-id>``` : cherry-pick range of commits

```git tag <tag-name> ``` : add a tag to a commit

``` git tag -d <tag-name>``` : remove a local tag.
***

#### Cleaning Up :

```git clean -f``` : remove untracked files

``` git clean -fd``` : remove untracked files and directory

***

``` git blame <file>``` : show who last modified each line of a file.





 
 



