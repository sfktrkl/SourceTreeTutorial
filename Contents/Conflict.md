<p align="right"><a href="../README.md#contents">Go back</a></p>

# Conflicts

Conflicts may happen when same content is edited by different people. When those changes must be merged, git is not capable of determining which version is correct the correct one. So, the developers must resolve that conflicts during the merging process.<br/>

When a conflict occurs in a merge operation, merge will be halted, and git will inform about the conflict.
```
git merge firstAndLastLine
Auto-merging Example.md
CONFLICT (content): Merge conflict in Example.md
Automatic merge failed; fix conflicts and then commit the result.
```
![iKjRR7pDMV](https://user-images.githubusercontent.com/48220015/111916655-fd05c380-8a8c-11eb-8a09-8a572e443788.gif)

It will also make additions to conflicted files about contents which are conflicting. Both versions of the content will be added to conflicting file inside some separators.
```
<<<<<<< HEAD
Content which is exist in the current branch
=======
Content which is present in the merging branch
>>>>>>> branch
```

The content inside those separators must be edited manually to resolve the conflict and merge operation must be continued.
```
(after resolving conflicts)
git add .
git commit
```
![TDd2JO2hC3](https://user-images.githubusercontent.com/48220015/111917882-41945d80-8a93-11eb-9b47-ab07fe524c3c.gif)


> Conflicts may sometimes be scary and confusing. Still, it is always possible to undo a merge and make a fresh start. It is also possible reorganizing the current or the target branch for smooth merge in case of very complicated situations.

### SourceTree resolving options

SourceTree offers to options to ease the resolving of the conflicts. Still, they are not capable of solving any kind of conflict, but they can be helpful in some situations. Those options can be found under `Actions -> Resolve Conflicts`.<br/><br/>
There are two choices to solve the conflicts,<br/>
`Resolve using 'Mine'`    - Current branch's content will be used to solve the conflict.<br/><br/>
![qcinoNfu2v](https://user-images.githubusercontent.com/48220015/111917329-6fc46e00-8a90-11eb-8b5b-1215825fd6aa.gif)
> Since current branch's content is used to resolve the conflict and there is no other change in the other files in the target branch, merge commit does not contain any changes.

`Resolve using 'Theirs'`  - Target branch's content will be used to solve the conflict.<br/><br/>
![94CS2BwzMU](https://user-images.githubusercontent.com/48220015/111917389-c03bcb80-8a90-11eb-9ca6-42490cb0f7d7.gif)

<p align="right"><a href="../README.md#contents">Go back</a></p>
