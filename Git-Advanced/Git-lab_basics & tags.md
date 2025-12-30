# migration from git-hub to git-lab

## git-lab :

- if you want to import repo : ```new project->import project-> git-hub->```
- give PAT (copy and paste from git-hub) - authenticate
```import --> go to profile```

- while we importing - its fails : in this situation we do :
  
--> + --> create blank project(create repo)

project name , un-check and create

> -- go to github - repo and copy https-link --> go to local : git clone --bare https-link --> ls and cd

(bare only download .git folder)

then : ```git remote add origin1 gitlab-link```
     : ```git push --mirror gitlab-link```

***

### tag : it will pointed to certain commit , we can give release note also in git-hub


```git tag v1.0```
```git push v1.0```

> do in main branch - git checkout main
```
git tag v2.0
git push origin v2.0
```
