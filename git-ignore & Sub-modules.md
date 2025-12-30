## git ignore : to ignore the file, folders etc.

```
code .gitignore 
```
>add abc.txt - add & commit --> create an abc.txt file it wont be added to stage area. it will ignore.
>>(use-case : we dont want to push build-files so we use this .gitignore )



## git submodules : repo inside a repo

> (if we want any reference of other repo)

```
git submodule add (repo-https-link) folder_name(if we want) 
```
>  create a submodule file (.gitmodules) and copy of repo also

>if we add . and push --> this repo will go to our branch
>> not as a copy as a reference 
>>> (it will point out the repo(path) - so not using the space)

>>for cloning :``` git clone --recursive httpslink```(we can take this also from our .gitmodule file-url)

>we can add multiple submodules.
