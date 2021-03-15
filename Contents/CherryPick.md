<p align="right"><a href="../README.md#contents">Go back</a></p>

# Cherry-picking, [git cherry-pick](https://git-scm.com/docs/git-cherry-pick)

Cherry pick is a very helpful tool that helps another commit to be appended to the current line of development. Using this tool any commit in any branch can be picked to the current branch with or without committing it. It can be helpful especially if a commit is made to a wrong branch and needs to be moved.
```
git cherry-pick <commit>
```
![MtjYsYnvht](https://user-images.githubusercontent.com/48220015/111910244-9fb04900-8a71-11eb-9198-54a3c05d187f.gif)


### Cherry-picking without making a new commit
With cherry-picking it is also possible moving the contents of the commit to working directory instead of making a new commit.
```
git cherry-pick --no-commit 3381106
```
![HrzgVM3ewh](https://user-images.githubusercontent.com/48220015/111910358-1d745480-8a72-11eb-91e1-a3382b092898.gif)


### Editing commit message
It is also possible editing the commit message before executing cherry-pick operation. Although SourceTree doesn't have an option to do that, it is offering an option to include original commit's id in the new commit.
```
git cherry-pick 3381106
(after it is done)

git cherry-pick --edit fcedf69
(edit the commit message, save and quit the editor)
```
![qrCF6YgGKc](https://user-images.githubusercontent.com/48220015/111910470-8bb91700-8a72-11eb-863c-4f6595b2e71a.gif)

<p align="right"><a href="../README.md#contents">Go back</a></p>
