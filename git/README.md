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
- 1- git init
- 2- Create repo on github
- 3- git remote add origin linktorepo.git
- 4- git push -u origin master
## Branch
  - get the curent Branch :
    ````
    git branch // return main or master
    ````
  - Create new Branch
    ````
    git branch branchName
    ````
  - Change Branch
    ````
    git checkout branchName
    ````
  - Remove Branch
    ````
    git branch -d branchName // Safe Delete
    git branch -D branchName // Forced Delete
    ````
  - Rename Branch Name
    ````
    git branch -m newBranchName
    ````
  - Merg and push
    ````
    git checkout main // go to main branch
    git merg newBranchName // merg main with new branch
    git push origin main // push main to origin repo branch
    ````
    <strong>Note</strong> : if we push directly the new branch to origin repo it will be push as a pull request
## Stash
the git Stash is like a virtual box or cloud space can save any files u want, and you can reset them for any time
Example :
- Create two files
  ````
  touch index.html style.css 
  ````
- check etat
  ````
  git status 
  // return will need to commit two files
  ````
- Add the files
  ````
  git add * // add this two files
  ````
- check status
  ````
  git status 
  // return that we need to push this two files
  ````
  but i don't want to push them, i need to save them and push another files for example
- Move to the stash
  ````
  git stash 
  // saved on stash andd we can't find them now in the local repo
  `````
- reset from stash to local repo
  ````
  git stash pop
  // move files from stash to local repo
  ````
  - git stash => move added files to the stash with default name
  - git stash save "text" => move added files to the stash with text name
  - git stash pop => move the last stash to the local repo
  - git stash apply => copy last stash from stash to local repo
  - git stash @{number of stash} => move specific stash
  - git stash drop => delete the last stash
  - git stash drop stash@{number} => delete specific stash
  - git stash show => show the content of last stash
  - git stash show stash@{number} show the .... of specific stash
  - git stash clear => clear and delete all stashs
## Restore and Clean
The restore command is used to restore files from stage
````
git restore -stage fileName or *
````
Clean is used to delete files
````
git clean -n
// return list of files will be deleted
git clean -f
// confirm the delete after see the files
````
## Reset the head
The head in the branch is the last commit.
so if we want to return to old version or delete a commit, we need to change the head.
for example :
- commit 1 : hash : 1234 HEAD
- commit 2 : hash : 4367
- commit 3 : hash : 8910
return to the commit 2 (delete the last commit) = (change the head)
````
git reset --hard hashOfCommit
git reset --hard 4367
git push --force
````
## ignoring files and directories
Some times we need to not push some files 
like .log files or some directories like nodu_module directory.
to doing that we need to creat .gitignore file
and add names of files or derictories on this file
<strong>.gitignore file :</strong>
`````
*.log // ignore all .log files
!vip.log // not ignore this file
ds_store // ignore ds_store
node_module // ignore directory
````
