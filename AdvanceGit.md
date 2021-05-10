Now of we have a main branch with some commit and now created a new branch feature and developed further on feature and at same time main brach is also get commited by teamates and now you are about to merge your branch and if we do so we will basicaly merge the commits of feature branch to main to keep the commit in unmixed to main branch we can squash the feature branch inito a single commit and then merge it.
`git merge --squash feature`
this will merge the feature branch onto main branch without merging its commits into main branch.
