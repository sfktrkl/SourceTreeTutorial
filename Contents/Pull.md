<p align="right"><a href="../README.md#contents">Go back</a></p>

# Pulling, [git pull](https://git-scm.com/docs/git-pull)

Pull command is used to download the content from a remote repository and update the local repository. It is a combination of [fetch](Fetch.md#fetching-git-fetch) and [merge](Merge.md#merging-git-merge) commands. Since, the purpose of fetching is updating the remote tracking branches without merging, merge command is completing the operation when pull command is used so local repository can match with the remote.
```
git pull <remote>
```
![7u117Ct5Jf](https://user-images.githubusercontent.com/48220015/111880863-d24d3980-89be-11eb-873e-9196ebf4fddf.gif)

### Pulling via merge
As default pull command is a combination of fetch and merge commands. Due to that merge command, after content is downloaded new merge commit will be created and HEAD will be updated to that point.
```
git pull origin

(equivalent)
git fetch origin
git merge origin/master
```
![ol2gLODyTD](https://user-images.githubusercontent.com/48220015/111880993-89e24b80-89bf-11eb-8572-ddaa8fc81b7d.gif)


### Pulling via rebase
To be able to avoid creating unnecessary merge commits and keeping history linear, `--rebase` option can be used. This option will [rebase](Rebase.md) changes instead of merging them after fetching remote branches. Since, it will move entire branch, it will rewrite the history by creating new commits for each commit in the original branch.
```
git pull --rebase origin

(equivalent)
git fetch origin
git rebase origin/master
```
![yIbQE3tQ9M](https://user-images.githubusercontent.com/48220015/111880995-8a7ae200-89bf-11eb-8dda-5557379947bf.gif)
>  To avoid typing `--rebase` option each time while using terminal it can be set as default.
>  ```
>  git config --global pull.rebase true
>  ```

<p align="right"><a href="../README.md#contents">Go back</a></p>
