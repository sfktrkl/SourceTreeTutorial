<p align="right"><a href="../README.md#contents">Go back</a></p>

# Branches, [git branch](https://git-scm.com/docs/git-branch)

Branches helps creating an independent line of development so without messing with the main line anyone can do their work and merge these to main line later.
Creating a branch or making changes in a branch will not affect the main line or a remote unless it is merged to main line or pushed to a remote.<br/>


### List of branches
```
git branch
```
List of the branches can be seen in SourceTree under `Branches`.


### Creating a branch
```
git branch <branch>
git checkout <branch>
```

SourceTree will automatically checkout to newly created branch when `Checkout New Branch` option is enabled in `Branch` popup.<br/><br/>
![cc5XwhndEf](https://user-images.githubusercontent.com/48220015/111877387-37e7f880-89b4-11eb-802d-29d3b02ce3e2.gif)

### Deleting a branch
Any local or remote branch (even master/main branch) can be deleted whenever it is needed.<br/>
Once a work is completed and changes are merged to the main line, it is recommended to delete both local and remote branches.<br/>
> Do not forget to checkout to another branch before deleting a branch.
```
git branch -d <branch>
git push -d origin <branch>  or  git push origin :<branch>
```
![rAEKLHDnBW](https://user-images.githubusercontent.com/48220015/111877398-49310500-89b4-11eb-865c-33be39feff56.gif)
> A remote branch can also be deleted with the same steps in SourceTree through `Remotes`.

If a branch has unmerged changes, it should be force deleted to get rid of all commits made in that line of development.
```
git branch -m <branch>
```
![UKriB77fEB](https://user-images.githubusercontent.com/48220015/111877451-82697500-89b4-11eb-9d73-863a5087c821.gif)

<p align="right"><a href="../README.md#contents">Go back</a></p>
