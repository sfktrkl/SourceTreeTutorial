<p align="right"><a href="../README.md#contents">Go back</a></p>

# Stashing, [git stash](https://git-scm.com/docs/git-stash)

Stashes can help to switch between works by saving the changes made to working copy temporarily. So, when it is needed to work on an urgent issue, local changes can be stored temporarily to used them. Since after creating a stash working copy will be cleaned, it will be possible to switch between works easily.
```
git stash  or  git stash push
```

Stashes can be listed according to their hash to later apply or delete them.
```
git stash list
```

In SourceTree, they will be listed under `Stashes`.<br/><br/>
![2ZJBjlBc6i](https://user-images.githubusercontent.com/48220015/111874104-afae2700-89a4-11eb-82e8-100f63cf4e63.gif)

### Keeping staged changes while creating a stash
It is possible keeping staged changes while creating a stash.
```
git stash --keep-index  or  git stash push --keep-index
```
![KpYLq7XIK0](https://user-images.githubusercontent.com/48220015/111874649-32d07c80-89a7-11eb-8bf9-9eaa884f27fa.gif)

### Applying stashes
They can be re-applied later to the working copy.
```
git stash apply stash@{n}  or  git stash apply n
```
![9QqpPbXbdW](https://user-images.githubusercontent.com/48220015/111874201-1fbcad00-89a5-11eb-8b27-011c86541b46.gif)

### Deleting stashes
Stashes can be deleted just after applying them.
```
git stash pop stash@{n}  or  git stash pop n
```
![fHqLqpQMZu](https://user-images.githubusercontent.com/48220015/111874311-bee1a480-89a5-11eb-80a3-83e0c8030f3a.gif)

Or they can be deleted directly if they are no longer needed.
```
git stash drop stash@{n}  or  git stash drop n
```
![bsSZHf18pK](https://user-images.githubusercontent.com/48220015/111874463-75458980-89a6-11eb-8d03-d0e96f4c2710.gif)

<p align="right"><a href="../README.md#contents">Go back</a></p>
