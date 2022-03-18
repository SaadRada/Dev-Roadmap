# git Commands
![git](https://www.wissenschaft.com.ng/wp-content/uploads/2021/02/git_banner.png)

Git is Distributed Version Control System Write in C, Shell, Perl, Tcl on 2005 By Linus Torvalds

- Repository : A software repository, or "repo" for short, is a storage location for software packages
- Branch : new/separate version of the main repository.
- Local Repo : local repo in my computer
- Remote Repo : the original repo in github for example
- Commit : snapshot or Checkpoint in Local Repo
- Clone : From Local or Remote 
- Push : Upload local changes to Remote
- Pull : Load changes From Remote to local
- Pull Request : Tell other About Changes to Pull it from local to Remote

![git](https://miro.medium.com/max/800/1*ZG8OzO2oTPi6cwm_e1h7rw.png)

## Clone
  ````
  git clone url
  ````
## Status
compare local repo with the remote repo
  ````
  git status
  ````
## Add
Prepare file to push them
  ````
  git add fileName
  git add * // to add all files
  ````
## Reset
Reset Added File
  ````
  git rest head fileName
  git reset head * // to reset all added files
  ````
## Commit
  ````
  git commit -m "message"
  ````
## Branch & Remote
  ````
  git branch // Master
  git remote -v // Origin
  ````
## Push
push from local to remote repo
  ````
  git push remoteName brancheName
  git push origin master
  ````
## Pull
load from remote to local repo
  ````
  git pull origin
  ````
## Config
  - get user email : git config --global user.email
  - get user name : git config --global user.name
  - set user email : git config --global user.email "mail.com"
  - set user name : git config --global user.name "saad"
## init
folder to local repo
  ````
  git init
  ````
## Create Repository From Existing Project
1- git init
2- Create repo on github
3- git remote add origin linktorepo.git
4- git push -u origin master