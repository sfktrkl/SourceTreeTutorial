<p align="right"><a href="../README.md#contents">Go back</a></p>

# Resetting, [git reset](https://git-scm.com/docs/git-reset)

Resetting tool is a very powerful tool which may help when it is needed to revert one or multiple commits done. Using reset, a commit can be removed either by keeping its changes or without keeping its changes. It may also help combining commits together or returning to a previous state.
```
git reset
```


### Soft reset
Soft resetting is especially helpful when a commit must be reverted, but the changes are still needed. It allows keeping the changes by staging them so it means that it will not reset the index which is the staging area.
```
git reset --soft HEAD^  or  git reset --soft HEAD~1
```
![UQQujm6W5M](https://user-images.githubusercontent.com/48220015/112143410-e1173480-8be8-11eb-897d-994840e00350.gif)


### Combining changes using soft reset
Since soft reset option can be used to remove a commit by keeping its changes and reset operation allows selecting how many commits will be discarded, soft reset can also be used to combine changes of multiple commits by discarding them and keeping their changes.
```
git reset --soft HEAD~2
```
![lqytaWiqFM](https://user-images.githubusercontent.com/48220015/112143590-250a3980-8be9-11eb-92aa-c9f93745831c.gif)


### Mixed reset
Mixed reset has a similar behavior with soft reset except it also resets the index. So, it will not keep the changes reset as staged, it will keep them in working directory. Hence, changes must be staged again to make a new commit. It may be helpful if commit reset contains many changes which needs to be separated anyways.
```
git reset --mixed HEAD~3
```
![PsbrNGLTpb](https://user-images.githubusercontent.com/48220015/112144279-0b1d2680-8bea-11eb-9cd9-9b58720e0561.gif)


### Hard reset
When a committed change is no longer needed or when it is committed to a wrong place it is possible to discard those changes with the hard reset.
```
git reset --hard HEAD~1
```
![ykAbpYP24d](https://user-images.githubusercontent.com/48220015/112140709-6bf63000-8be5-11eb-8c14-6a07f727551f.gif)


### Undoing a hard reset
It is possible undoing the reset if something is accidentally discarded. It does not mean that every reset operation can be undone since git is using a garbage collector to optimize the local repository. It may not be possible undoing a reset if it is done quite a long time ago. [Terminal](Terminal.md#terminal-in-sourcetree) can be used to undo a reset operation and to do that it has to be known that which listing in `git reflog` will be used.
```
git reset --hard HEAD~1
git reflog
(determine listing which needs to be used)
git reset --hard HEAD@{1}
```
![JnMizTai5a](https://user-images.githubusercontent.com/48220015/112145811-e32ec280-8beb-11eb-81be-aae5f03949ba.gif)

<p align="right"><a href="../README.md#contents">Go back</a></p>
