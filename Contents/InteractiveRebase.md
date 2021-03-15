<p align="right"><a href="../README.md#contents">Go back</a></p>

# Interactive rebase, [git rebase](https://git-scm.com/docs/git-rebase)

Sometimes it is needed to revise the commit history. When this is needed, it is possible to rewrite the commits that are already happened to make them happen in a different way. It is possible rewriting the commit messages, squashing couple of them, reorganizing their order and even deleting them.<br/>

[Amend](Commit.md#amend) is a one way to do that for the last commit. It helps changing the message and content of the last commit.
```
git commit --amend
```

Another way is the interactive rebasing and it also makes possible modifying more than one commit at a time starting from the last n commit.
```
git rebase -i HEAD~n
```

This command must be followed up with certain commands like,
```
p, pick = use commit
r, reword = use commit, but edit the commit message
e, edit = use commit, but stop for amending
s, squash = use commit, but meld into previous commit
d, drop <commit> = remove commit
and more...
```

Since SourceTree offers a user interface to run these commands. It is much easier to execute them.
```
git rebase -i HEAD~2
```
![KdUdfBdA6O](https://user-images.githubusercontent.com/48220015/111906835-a59f2d80-8a63-11eb-99fd-7102c71ea465.gif)

### Squashing commits

With interactive rebase it is possible to take couple commits together and squash them to one.
```
git rebase -i HEAD~2

(change pick keyword to squash or s in second commit)
pick 3381106 Update first line of the Example.md
squash 34357d3 Update second line of the Example.md

(save and quit the editor twice)
```
![ioVwvaDKWW](https://user-images.githubusercontent.com/48220015/111907117-fbc0a080-8a64-11eb-9933-69f682464ece.gif)


### Editing commit messages
It is also possible editing a commit message through interactive rebase.
```
git rebase -i HEAD~2

(change pick keyword to reword or r in second commit)
pick 3381106 Update first line of the Example.md
reword 34357d3 Update second line of the Example.md

(save and quit the editor)
(edit message and save and quit the editor)
```
![Dz3dEsTXug](https://user-images.githubusercontent.com/48220015/111907312-c9fc0980-8a65-11eb-944e-4f97c27e7bdb.gif)


### Deleting commits
If it is needed to get rid of a commit, it can be deleted.
```
git rebase -i HEAD~2

(change pick keyword to drop or d in second commit)
(Or delete the commit's line)
pick 3381106 Update first line of the Example.md
drop 34357d3 Update second line of the Example.md

(save and quit the editor)
```
![T8MYB4uKR2](https://user-images.githubusercontent.com/48220015/111907401-30812780-8a66-11eb-9438-f8cf27c3dc29.gif)


### Reordering commits
Interactive rebase can be used to reorder the commits.
```
git rebase -i HEAD~3

(arrange the order of the commits)
pick 3381106 Update first line of the Example.md
pick 34357d3 Update second line of the Example.md
pick 53d913e Update Example.md

(save and quit the editor)
```
![NCDUrrwhO3](https://user-images.githubusercontent.com/48220015/111907601-214ea980-8a67-11eb-94bf-88096a294da1.gif)


### Multiple operations can be done at the same time
It is also possible executing multiple operations at the same time with interactive rebase.
```
git rebase -i HEAD~3

(arrange the order of the commits)
(change pick keyword to reword or r in first commit)
reword 3381106 Update first line of the Example.md
pick 34357d3 Update second line of the Example.md
pick 53d913e Update Example.md

(save and quit the editor)
(edit message and save and quit the editor)
```
![ubT3q8G52E](https://user-images.githubusercontent.com/48220015/111908241-899e8a80-8a69-11eb-8c28-571ecaa5fda7.gif)


### Aborting rebase
While doing interactive rebase operations, it is possible that the changes made cause conflicts. In this case, git will fail to apply the changes and give a conflict message for a certain step. If it is needed, rebase operation can be aborted to revert the files to their version before interactive rebase.
```
git rebase -i HEAD~2

(arrange the order of the commits)
pick 34357d3 Update second line of the Example.md
pick 3381106 Update first line of the Example.md

(save and quit the editor)

(this will give a conflict)
Could not apply 34357d3... Update second line of the Example.md
Auto-merging Example.md
CONFLICT (content): Merge conflict in Example.md

git rebase --abort
```
![Mv2tUR41wD](https://user-images.githubusercontent.com/48220015/111907776-ded99c80-8a67-11eb-9787-ef4fce028246.gif)


### Continuing rebase
It is also possible continuing the rebase after solving the conflicts.
```
git rebase -i HEAD~2

(arrange the order of the commits)
pick 34357d3 Update second line of the Example.md
pick 3381106 Update first line of the Example.md

(save and quit the editor)

(this will give a conflict)
Could not apply 34357d3... Update second line of the Example.md
Auto-merging Example.md
CONFLICT (content): Merge conflict in Example.md

(solve the conflicts in the files)
git add .
git rebase --continue
```
![iXoUWn4d58](https://user-images.githubusercontent.com/48220015/111908989-7345fe00-8a6c-11eb-9d6c-9f20cba4d23e.gif)

Since SourceTree says further steps must be manually done after getting a conflict during the interactive rebase. Conflicts in the files has to be solved and [terminal](Terminal.md#terminal-in-sourcetree) has to be used to manually add changes and continue to rebase.<br/><br/>
![EtvrVUYrNn](https://user-images.githubusercontent.com/48220015/111909102-f7988100-8a6c-11eb-850b-2c86a55f4780.gif)


> It must be noted that, those rebase operations are editing the local repository. So, when a rebase operation done in a local branch which has a remote needs to have the same changes, those changes has to be [force pushed](ForcePush.md#force-push-git-push) to the remote.

<p align="right"><a href="../README.md#contents">Go back</a></p>
