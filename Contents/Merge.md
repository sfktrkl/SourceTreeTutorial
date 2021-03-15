<p align="right"><a href="../README.md#contents">Go back</a></p>

# Merging, [git merge](https://git-scm.com/docs/git-merge)

Purpose of merging is combining multiple development lines which have independent histories together to same branch. After a merge, a new single commit which contains all the changes from the target branch, will be created.
```
git merge <branch>
```
![1U659i4LJN](https://user-images.githubusercontent.com/48220015/111914561-89ab8400-8a83-11eb-8eff-51ee0a1243f9.gif)


It may require some preparation since during the merge operation with two branches which changes the same part of the file git won't be able to apply the merge operation and will request conflicts to be solved.<br/>
Some of the basic operations to resolve conflicts are included in the SourceTree.<br/>
They can be found in the toolbar under `Actions -> Resolve Conflicts`.


### Aborting merge
When a merge operation halted due to the merge conflicts, merge operation can be aborted to return to the state before starting merge. So, that target or receiving branch can be arranged further for a smooth merge.
```
git merge --abort
```
![7rJ2HfcwnH](https://user-images.githubusercontent.com/48220015/111915417-3804f880-8a87-11eb-83a6-c254c29e6180.gif)


### Continuing merge
It is also possible fixing the conflicts manually and continuing the merge operation.
```
git merge --continue
```
![zdFjXPObWn](https://user-images.githubusercontent.com/48220015/111915641-53243800-8a88-11eb-8e9a-4781dcafca73.gif)
> Further details about solving a conflict can be found [here](Conflict#conflicts).

<p align="right"><a href="../README.md#contents">Go back</a></p>
