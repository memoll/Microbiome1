"How to start using git"
- Mona Parizadeh
- November 2017

#Configuration:
git config --global user.name “username”
git config --global user.email “toto@email.com”
git config color.ui "auto"
git config core.editor "nano -w"
git remote set-url origin http://github.com/username/
git config --list

#Initiation (in bash)
git init Myproject #iniates and creates a new repository
rmdir MyProject #not empty!!
cd MyProject
ls #shows empty
ls -a #shows hidden files
rm -rf .git #remove hidden files
cd ..
rmdir MyProject #done

#R-project
Open new project in R_projects (Microbiome)
Open new file in R_projects (phyllosphere) and write down somthing in the file:
phy = read.table("~/Phyllosphere.txt")

#Commiting (in bash)
git status
git add -A #adds all files to the git, these are not permanant yet and need to be commited
git commit -m "start Microbiome project"

#Sending to the remote server
git remote add origin http://github.com/memoll/Microbiome1/
git push origin master #to send my modifications to the remote server
# if push doesn't work, we need to set url to the new repository:
git remote –v #to verify
git remote set-url origin http://github.com/memoll/Microbiome1/ #copy the http or ssh from the server

#Pull file from the remote server
create new file on github (protocol)
git pull origin master #to receive all the modifications other than local

#Undo
nano methods : add "qPCR" and save
git checkout methods #to erase what hasn't being commited yet

#Create new branch: no interruption with the same files on the master branch
git checkout -b newBranch #switches to the new branch
nano file(protocol): make a change, save, add, commit:
git add protocol
git commit -m "message"
git checkout master #switches to branch master #no changes yet in the branch master 

#Merge newBranch and branch master
git merge newBranch/file file #to merge files, no need to commit again, only send to the remote server (push):
git push origin master
git branch -d newBranch #to delete the newBranch





 



