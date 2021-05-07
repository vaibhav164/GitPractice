# GitPractice

## Basic Commands:-

1. **clone** it is used to clone repo from Remote directory to your local system to use or further edit it.
2. **add** use to add the edited file into staging area.
3. **commit** to save the edited changes of filof local system.
4. **push** upload the commited file to remote Repository.
5. Download changes from remote repo to your local machine.

---

> Keep Hus

**git add .** the dot in this refered as period an it will select all the files in the git repo to add to staging area.

### SSH keys

to generate SSH key to keep the repo authenticated us command
`ssh-keygen -t rsa -b 4096 -C "your-email-address@gmail.com"`
ssh-keygen generates the ssh key in local system.
-t rsa -b sets the type of encryption
4096 -C sets the lenghth of encryption
and at the end add your github email address

**git push**
Now command git push -u origin master
here -u refers to upstream to make the pushing repo of remote as default i.e., after this command we can just type git push to push our local repo to remote.

# git pull:-

this will save all the changes happed to remote repo into our local repo snice the last time we had push our repo to the Remote.

**git clone:-**
the syntax is `git clone <URL> <where to clones>`

# Branching:-

to make branch commadn is
`git checkout -b branch-name`
here checkout means that we are switching fro the current branch to new brach of name `branch-name`
and -b branch-name will create a new git branch for e.g.,
`git checkout -b apple` this will create a new branch of name apple and switch to it from current branch

**git diff**
to chack out difference between to branches we use git diff command
e.g., `git diff apple` this will show the difference between the current branch and apple branch.

**pushing new branch created to local system to remote repo:-**
`git push -u origin apple`
the above command will push new branch to the remote repo of name apple

**git commit -am "Commit msg"** this command is use to add and commit the edited file at same time but it applies for only modified files only now to the new added files.

### Git Add:-

1. git add -A this command stages all the changed files of our projects and to role back it jus type command **git reset**.
   if we are in some other folder of our project in cmd and typed the command git add -A it will still add all the files of the projects into the staging area.

2. `git add -A mu_dir/` this will a all the files of my_dir directory to the staging area. it is as same as (`git add my_dir`) command.
3. `git add --no-all my_dir` this will add all the files from the my_dir except the deleted files.

4. `git add -u` this adds all the modified files ie updared files or deleted files except the untracked files id newly added files from the entire project.

5. `git add -u my_dir` this will add all files from my_dir except untrracked files.

6. `git add .` this works the same as `git add -A` when we are in top directory but when we are in subdirextory it will only add all files of that sub Directory unlike `git add -A` in sub-directory.

7. `git add *` this command is not that good to be used as it will add the file that are shown in Directory i.e it will not be able to track deleted and Hidden files.

- the command in sub dirextory will add all the staged files except the deleted and hidden file of that perticular directory not of it further sub directory.

# Git Help

1. to get help regarding any topic of git type simple command git --help
2. to get help for specific keyword type `git config --help` or `git help config` this will show the list about config.

## Git ignore:-

1. For the people to not view out personal referance files of our project we can arrange the file system which gets ignored by git using git ignore command
   `touch .gitignore`
   the above command will create a file as .gitignore file and then can be used to work

to make file ignored by git type simply the name of the file into thaht file and the git will ignore that file .

create the .gitignore file use gitbash after creating the gitignore file just enter the name of the file and git will ignore and will not be pushed to your remote repo.

## Git Reset:-

1. this command is used to reset the file from the staging area.

**git remote -v** this will tell us the location of the local and its respective remote repo.

**git branch -a** this will list the all branches of local and its respective repo.

# Deleting the merged Branch to the maste/main:-

1. to do so run command `git branch --merged` this will the that is the branch got merged to each other or not.
2. syntax to delete the branch is `git branch -d branch_name`
3. git command to delete a branch from remote repo `git push origin --delete branch_name`.
