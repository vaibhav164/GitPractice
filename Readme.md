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
