<p align="right"><a href="../README.md#contents">Go back</a></p>

# Staging, [git stage](https://git-scm.com/docs/git-stage)

Staging step helps cutting your changes into smaller pieces. So, while continuing making changes, it can help you to separate the changes you want to commit. It is most useful when there are too many changes and they need to be sorted out somehow.

```
git add  or  git stage
git restore --staged
```

In git and SourceTree there are several options to stage/unstage a file or a hunk.<br/><br/>
SourceTree offers these options through `History` and `File Status` windows.<br/><br/>
![uDBz70W4Tj](https://user-images.githubusercontent.com/48220015/111870427-bd0fe500-8995-11eb-897c-547a4caf51bf.gif)


### Stage/Unstage all files
When all changes are ready to commit, they all can be staged to make them ready to commit.
```
git add .
git restore --staged .
```
![ih3RJsXihS](https://user-images.githubusercontent.com/48220015/111870121-e0399500-8993-11eb-861b-269e048b668b.gif)


### Stage/Unstage a file
If it is needed to separate certain files from others to commit them, those files can individually be staged.
```
git add a.txt
git restore --staged a.txt
```

![8W6QEEU4ff](https://user-images.githubusercontent.com/48220015/111870154-1119ca00-8994-11eb-9ad2-3185ef37b5b8.gif)


### Stage/Unstage a hunk
If a file contains many changes or changes made in a file which has to be sorted or separated, those changes can be staged as hunks.
```
git add -patch Example.md  or  git add -p Example.md
```
This command will open up the patch mode, so it will be followed with certain commands like,
```
Stage this hunk [y,n,q,a,d,k,K,j,J,g,/,s,e,?]?

y - stage this hunk
n - do not stage this hunk
q - quit; do not stage this hunk or any of the remaining ones
a - stage this hunk and all later hunks in the file
d - do not stage this hunk or any of the later hunks in the file
s - split the current hunk into smaller hunks
and more...
```

In SourceTree file has to be selected first to view the diff, then the hunks can be staged/unstaged easily.<br/><br/>
![fAGtqwmgSu](https://user-images.githubusercontent.com/48220015/111870244-9ac99780-8994-11eb-8a82-7aeeebe2b270.gif)

It is also possible modifying the size of the hunks. Which is equivalent to `s` command in patch mode.<br/><br/>
![S3GPzTJ4gc](https://user-images.githubusercontent.com/48220015/111870319-1deaed80-8995-11eb-94e6-64e8305f7ea4.gif)
> Besides changing the hunk size and staging that hung, one or multiple lines can be selected and staged using the diff view.

<p align="right"><a href="../README.md#contents">Go back</a></p>
