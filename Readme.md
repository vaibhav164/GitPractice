# GitPractice

## Bbasic Commands:-

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

## UNdo the code :-

if we had codoed and we feel that we want to undo all the change from the file and want the earlier code use command `git checkout file_name`.

## Update the last commit message:-

if we want to edit the message of last commited file of the project use command
`git commit --amend -m 'new commit msg'` this will change the last commit msg and this it will cause change in the git hash as well as editing the git msg basicaly changes the git history.

## add more file to the commited repo after commit :-

if we ha already commited a repo but want to add more file to that then it can be done using
`git commit --amend` by this it should work but didn't for me.

the select edit in window instruction and after type **:** and **wq** and press enter to make it work and this will also change the git hash .

# Edit commit in wrong branch:-

## to brought the commit to other branch:-

use concept of Cherrypick for this fist copy ths hash of the commit that is to be transfered and then chackout from the branch to the branchi in whick you want to insert that copied commit and then add command `git cherypick <hash value of the commit>`

# Git Reset:-

1. there are three types of reset git reset soft, git reset hard, git reset mix

- **git reset --soft** this will reset the commit we did but will save the changes that where performed.
- **git reset** this will reset the commit and also unstage the changes that where made.

-**git reset --hard** this will completely wipe out the commit including the changes that where made. this reverse all the commit or wipe it out from the earlier commit except untacked files such as .gitignore.

To completely wipe the tracked or untracked file use command
`git clean -df` this will clean all the untracked files here in -df d stands for direactory an f for files.

## git reflog

the command `git reflog ` will show you the command is done on the repo

![Ref Log Example](./reflog)

## Undo the reset :-

to do this use command `git checkout <hasvalue from reflog of before the reset>`

but these reset files are retrived but for temporery basis whenever the git garbage collector will run it will remove to so to save it make a branch from that incident to same the undo of reset of it.

# git revert :-

it is used when we realy want to reset some commits but other people fromteam hai pulled it earliarly for this condition use git revert it crets a new commit to reverse the prvious commit by this wawe do not disturb the history of git remote repo.

its syntax is `git revert <has value ofthe commit which needs to be Undo>`

## Git diff between two different commits

syntax for it is as `git diff <hash of one commit> <hash of other commit>` this will shows the difference between the two different commits.

# git Stash:-

it used when we are not sure about whethere we should commit the change or need it wait further
using this we can save the change for temporary and can come back when feel require to commit and till then we can go further for development.
syntax `git stash save "messange whatever you wana type"`
after doinf this we can switch to other branch and work on other branch without commiting this stash one.

**git stash list** this command will provide the list of stash performed.

once we had done with our work and want to apply our stash to do it use command as
**git stash apply stash@{0}** this will apply the stash of index number 0 here stash@{0} is representing stash index number.

and if wana reset it again use command `git checkout -- .`
**remove a saved stash:-** for this apply command `git stash pop` this will grab a very first stash of stash list.
