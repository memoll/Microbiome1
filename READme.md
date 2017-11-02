## "How to start using git" 
- Mona Parizadeh
- November 2017

## Git info
- git --version
- git --help

## Configuration:
- git config --global user.name “username”
- git config --global user.email “toto@email.com”
- git config color.ui "auto"
- git config core.editor "nano -w"
- git remote set-url origin http://github.com/username/
- git config --list

## Initiation (in bash)
- git init Myproject #iniates and creates a new repository
- cd MyProject
- touch file.txt
- ls
- rm file.txt
- ls #shows empty
- rmdir MyProject #not empty!!
- ls -a #shows hidden files
- rm -rf .git #remove hidden files
- cd ..
- rmdir MyProject #done

## R-project
- Open new project in R_projects (Microbiome)
- Open new file in R_projects (phyllosphere) and write down somthing in the file:
- phy = read.table("~/Phyllosphere.txt")

## Commiting (in bash)
- git status
- git add -A #adds all files to the git, these are not permanant yet and need to be commited
- git commit -m "start Microbiome project"

## Sending to the remote server
- git remote add origin http://github.com/memoll/Microbiome/
- git push origin master #to send my modifications to the remote server

- If push doesn't work, we need to set url to the new repository:
- git remote –v #to verify
- git remote set-url origin http://github.com/memoll/Microbiome/ #copy the http or ssh from the server

## Pull file from the remote server
- create new file on github (Protocol)
- git pull origin master #to receive all the modifications other than local

## Undo
- nano methods : add "qPCR" and save
- git checkout methods #to erase what hasn't being commited yet

## Create new branch: no interruption with the same files on the master branch
- git checkout -b newBranch #switches to the new branch
- nano file(Protocol): make a change, save, add, commit:
- git add Protocol
- git commit -m "message"
- git checkout master #switches to branch master #no changes yet in the branch master 

## Merge newBranch and branch master
- git merge newBranch/file file #to merge files, no need to commit again, only send to the remote server (push):
- git push origin master
- git branch -d newBranch #to delete the newBranch

## Merge two modifications on the same file
- modify the remote and local file(Protocol) in 2 different ways
- git add Protocol
- git commit -m "message"
- git pull origin master #merge conflict
- git fetch origin #to update the remote server
- git push origin master #rejected
- git diff #shows the conflict
- git merge #not possible and need to be fixed
- open file(less Protocol) #kept both modifications
- edit file(nano Protocol), save
- git add Protocol
- git commit -m "message"
- git push origin master

## Project Info
- git log #prints all the changes (when, who, what)




 



