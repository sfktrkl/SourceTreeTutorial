<p align="right"><a href="../README.md#contents">Go back</a></p>

# Pushing, [git push](https://git-scm.com/docs/git-push)

Push command is used to upload local changes to a remote. Unlike committing the purpose of `push` is updating the branches on remote. Hence, changes needs to be pushed have to be [committed](Commit.md#committing-git-commit) before. Pushing will make changes accessible to everyone which has access to this repository, so they can pull those changes.
```
git push <remote> <branch>
```
![qfCqIyHdj3](https://user-images.githubusercontent.com/48220015/111880630-a67d8400-89bd-11eb-9191-7f8bc35f048a.gif)


SourceTree also offers an option to push the changes to the remote just after committing them.
```
git commit -m "Update Example.md"
git push origin master
```
![u95mdS5OTW](https://user-images.githubusercontent.com/48220015/111880654-d62c8c00-89bd-11eb-8665-d0f8caee9860.gif)

> Before pushing to the remote always [pull](Pull.md#pulling-git-pull) from the remote to be sure about local repository is in sync with the remote repository. Doing this will help not ending up with merge conflicts and multiple heads.

<p align="right"><a href="../README.md#contents">Go back</a></p>
