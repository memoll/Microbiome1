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
git init Myproject #iniates and creates a directory
rmdir MyProject #not empty
cd MyProject
ls # nothing
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
git push origin master
# if push doesn't work, we need to set url to the new repository:
git remote set-url origin http://github.com/memoll/Microbiome1/



