<p align="right"><a href="../README.md#contents">Go back</a></p>

# Fetching, [git fetch](https://git-scm.com/docs/git-fetch)

Fetch can be used before doing pull to check whether there are new works done by other people. Fetching will update all remote-tracking branches without merging those changes. So, its purpose is just to see whether there are new changes or not. Hence, it is recommended to fetch and pull before pushing to a remote to avoid accidents.
```
git fetch <remote>
```
![I8SXIGB8yD](https://user-images.githubusercontent.com/48220015/112172832-18480e80-8c06-11eb-92ea-30def5b7d361.gif)


### Fetching from all remotes
Since, it is possible having more then one remote repository, fetcing has an option to retvieve information from all registered remotes and their branches.
```
git fetch --all
```
![U2yLP4k2ET](https://user-images.githubusercontent.com/48220015/112173038-475e8000-8c06-11eb-91af-862ceb5553ad.gif)


### Pruning tracking branches
During the development it is possible that some of the branches may get deleted. To be able to clean those outdated branches `--prune` option can be used during fetching.
```
git fetch --prune
```
![Jm55muWLwE](https://user-images.githubusercontent.com/48220015/112174210-48dc7800-8c07-11eb-8314-0160e57d992a.gif)


<p align="right"><a href="../README.md#contents">Go back</a></p>
