Now of we have a main branch with some commit and now created a new branch feature and developed further on feature and at same time main brach is also get commited by teamates and now you are about to merge your branch and if we do so we will basicaly merge the commits of feature branch to main to keep the commit in unmixed to main branch we can squash the feature branch inito a single commit and then merge it.
`git merge --squash feature`
this will merge the feature branch onto main branch without merging its commits into main branch.

to complete the process we have to rebase the branch `git rebase main`
this command will be executed from feature branch.

### Cherry picking:-

It is used to bring a commit of some other branch of a project to our branch.
we can cherry pick one or many commits.

## Git Tags:-

It is used to when you want to create a release point for a stable version of our code .
OR when we want to create a Historic point of our code so that whenever it is required we can rerun or access it .

To create a Tag there are some steps to follow which are as follow:-

1. Chechout to the branch where you want to create a tag.
2. Create a tag with a tag-name syntax is as `git tag <tag name>`. eg git tag Version-1.0
   we can also annotated tag using -a syntax is as `git tag -a <tag name> -m "Some msg for the tag as annoted"`.
3. to show list of tags in we created syntax is `git tag`.
4. to show the tag with tag name syntax is `git show <tag-name>`.
5. `git tage -l "v1.*"` this will show all the tags staring with name v1 ,
6. To push tags to the remote repo use the syntax as `git push origin <tag-name>`. To push all tags to remote repo use command `git push --tags` OR `git push origin --tags`
7. To delete a Tag use command `git tag -d <tag-name>` OR `git tag --delete <tag-name>`.
8. To delete tag from remote repo `git push origin -d <tag-name>`
9. To delete multiple tags `git tag -d <Tag-name1> <tag-name2>` this will delete two tags and so on we can mention all the name that needs to be deleted.
10. **Checkingout from Tag**:-
    we cannot checkout from a tag but we can create a branch from a tag point and checkout to that created branch.
    to do so `git checkout -b <branch-name> <tag-name>`.
11. **to create a tag from some past commit** syntax `git tag <tag-name> <raferance of commit>`.

# Rebase

this is use to adkjust the position of the previous commits from the current heade we can change the positions .
