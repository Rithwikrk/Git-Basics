# hooks :

### PAC [Personal access tokens] :

- Definition : Whenever we used https - we need a token to push it (in ssh we dont need any)

- User settings --> developer settings --> tokens(classic) --> Generate new token

>note : give some name 
>>give all the permission


###### Situation : store the password and token in code and push it in the project  (copy the token and paste in to code)

> whenever the commits need to check & check the file(code) contain any password or token before pushing in to remote repo : ```we use hook```
> + ```ls  -la``` (list hiddens files)
> + ``` .git ```- folder that contain all our branches, commit info and passwds,etc
> ```--> cd .git --> ls```
> ```cd hooks --> ls --> .sample ```- so we need to enable the file ( ie, change .sample to normal )

> - if i want to run something before i commit :
> - check precommit and perform this ( somany options are there like post/pre push, post/pre commit,etc)

> - to enable it : mv pre-commit.sample pre-commit (basically remove the .sample format to normal file)
> ls --> and check its removed or not
> Now these scripts will execute before commiting in local.
>> ```code pre-commit ``` - to check whats inside the code 

***

#### exercise :-

##### Scenario : remove and clear all the code in the pre-commit file,

add : 
```
#!/bin/sh
echo " this is pre-commit hooks"
```
>  (note : whats the first cmnt in shell scripting - #!/bin/sh)

- save & cd .. .. --> go back

> (imp note : .git changes dont push )
```
git status
git add .
git commit -m "test hooks" 
```
> now we can see the changes


#### hooks - concept by using with if you want to execute before any events/activities happend.


### Scenario/Ques : if any pat tokens are there in code , dont let them commit and come to exit :

> open pre-commit (.git file) - add the shell script for identify the pat-tokens ( take the script from chatgpt)
>> - save the pat-token in code
>> - git status --> git add . --> git commit -m "test hooks" -it wont commit due to the pat-token in code itself.

***

##### shell script code :
```
#!/bin/bash

echo "scanning"
for file in $(git diff --name-only --cached)
do
   echo "scanning for secrets in $file"
   secret_found=$(grep "ghp" "$file")
   if [ -n "$secret_found" ]; then
   echo "secret found in $file"
   exit 1
   fi
done
```
****

```
git status
git add .
git commit -m "test hooks" 
```
> -- now we can see the changes
>> if its working : then remove and test it out again.
