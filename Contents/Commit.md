<p align="right"><a href="../README.md#contents">Go back</a></p>

# Committing, [git commit](https://git-scm.com/docs/git-commit)

It is simply used to save changes to the local repository. Commits can be though as snapshots of a project in a certain timeline. Also, commit command will not save changes to remote, it will affect only the local repository. Since git can't know which changes needs to be saved, files and changes which needs to be saved has to be [staged](Stage.md#staging-git-stage) before committing.
```
git commit
```
It is expected that a commit to have a commit message, so it will open file editor to write the commit message.<br/>
Also `-m` option can be used to set a commit message.
```
git commit -m "Update Example.md"
```

In SourceTree, using `File Status` window, changes can be committed. It is allowing to set a commit message.<br/><br/>
![0x3kqo2Nc9](https://user-images.githubusercontent.com/48220015/111871176-e03c9380-8999-11eb-9779-a23c28de0433.gif)

SourceTree is also allowing committing with an empty commit message. It automatically writes a commit message as `no message`.<br/><br/>
![bPKc163Ljv](https://user-images.githubusercontent.com/48220015/111871280-23970200-899a-11eb-9fb2-7b921de25ed2.gif)

### Amending latest commit
This option will rewrite the last commit with the current changes.
```
git commit --amend
```
> Note that, if the last commit is already pushed to the remote, commit has to be [force pushed](ForcePush.md#force-push-git-push).

In SourceTree, this option can be found under the `Commit Options`.<br/><br/>
![kgg9mE2DrP](https://user-images.githubusercontent.com/48220015/111871499-77eeb180-899b-11eb-8eb4-b989f790e169.gif)

<p align="right"><a href="../README.md#contents">Go back</a></p>
