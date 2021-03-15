<p align="right"><a href="../README.md#contents">Go back</a></p>

# Force push, [git push](https://git-scm.com/docs/git-push)
During the development, it may be needed to rewriting or changing commits which are already pushed. Commands like `git rebase`, `git squash` and `git commit --amend` have capabilities to rewrite and change a commit. Since, these commands will create new commits and a new history instead of just changing them, remote history must be rewritten. So, `git push` will fail, and those changes must be pushed by forcing them.
```
git push --force  or  git push -f
```
![vP9RqcSsMD](https://user-images.githubusercontent.com/48220015/111882028-4dfdb500-89c4-11eb-81a9-5ab3955ff3ec.gif)


### Getting changes after someone force-pushed to a branch
Since, force push operation can be done by anyone which has access to the remote repository and its branches. It is possible that encountering with a completely different history after fetching the remote. To get those changes from the remote and update the local repository, it is possible removing local branch and getting those changes by checking out the branch again. If there are changes in the working copy, it is also possible stashing them to use them after updating the local branch.
```
git stash
git checkout master
git branch -D myBranch
git checkout myBranch
git stash apply stash@{0}
```
![mfjXYWQVs8](https://user-images.githubusercontent.com/48220015/111882229-910c5800-89c5-11eb-9e4a-fe01d05b2642.gif)

<p align="right"><a href="../README.md#contents">Go back</a></p>
