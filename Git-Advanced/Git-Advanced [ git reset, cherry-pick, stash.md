# git reset -  undo any commit that created in our local ( --mixed)

- ```git reset Head~1``` - remove the last commit
 
 - ```git reset ---mixed``` ( git reset) : remove the commit ; but file changes not removed.

- ```git reset --hard```                 : commit removed ; file changes also be removed in local.

eg : [ ```git reset --hard head~1```]

- ```git reset --soft ```                :  remove the commit ; files changes will go to staging area.
  
[Unstage :- git restore --staged file : to unstage (to que)] then again commit the other file and push.

[Remove from stage :- or we can use : git rm --cached file]

***

> important :
## git cherry-pick

```git cherry-pick``` : take the certain commit from any other branch to which ever the branch you required

if we dont want the cherry-pick req : ``` git cherry-pick --abort```


## git rm --cached file : for removing files from stage area

## git diff : check the changes b/w 2 commits ( red - removed ; green - added )

also used to check the diff in files : git diff file_name
***

rarely use this cmd : 
```
git stash 
git stash apply
```
Use-case : 

if we are creating a branch and dont want the local copy changes , only need the master copies :

do - ```git stash```

   - ```git checkout -b new_branch```
     
all current changes in local go to a index state WIP.

if we need that change again in do - ```git stash apply```

[ i done some changes (all changes will be there in some temporay cache-index state), i dont want now, i will requires it later : these kind of situation git stash come to picture]

