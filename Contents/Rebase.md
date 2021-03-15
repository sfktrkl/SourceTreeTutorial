<p align="right"><a href="../README.md#contents">Go back</a></p>

# Rebasing, [git rebase](https://git-scm.com/docs/git-rebase)
Rebase is one of the two git commands which is used to move or combine a series of commits to a new base. It is especially helpful to keep history clean and linear because it will not create any additional [merge](Merge.md#merging-git-merge) commits. Also, unlike merging it will rewrite the commit history by creating new commits for each commit in the original branch. Hence, if keeping the history of the commits is a priority, merge command should be used.
```
git rebase origin/master
```
![KT6zIG3ass](https://user-images.githubusercontent.com/48220015/111881734-f579e800-89c2-11eb-9031-2f0ef36cb4af.gif)

### Updating local repository with rebase
When pull command is used with `--rebase` option, [pull](Pull.md#pulling-via-rebase) command becomes a combination of [fetch](Contents/Fetch.md#fetching-git-fetch) and rebase commands. Hence, if branches are already fetched, it is possible to use rebase command to get the contents from the remote repository and update the local repository.
```
git rebase origin/master
```
![GL4imaMVZa](https://user-images.githubusercontent.com/48220015/111881814-543f6180-89c3-11eb-9949-134ef32d6de0.gif)

Before rebasing either commit changes or stash them.
```
git stash
git rebase origin/master
git stash pop stash@{0}
```
![aAKnsSfkKF](https://user-images.githubusercontent.com/48220015/111881900-c021ca00-89c3-11eb-846f-7ba000f5f9c5.gif)


### Rebasing remote tracking branches
Rebase is rewriting the commit history, when a remote tracking branch is rebased it will not possible simply pushing these changes since commit history is rewritten. Hence, changes has to be [force pushed](ForcePush.md#force-push-git-push) to update the remote branch.
```
git checkout myBranch
git rebase origin/master
git push --force
```
![1Hy4FiCHL9](https://user-images.githubusercontent.com/48220015/112310054-2c971480-8cb5-11eb-9834-7dc6e248c3d4.gif)

<p align="right"><a href="../README.md#contents">Go back</a></p>
