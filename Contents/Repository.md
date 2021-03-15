<p align="right"><a href="../README.md#contents">Go back</a></p>

# Repository

Repository contains all files and folders in a project including their all history.
- Local repository: Simply the project's location in the local machine which git is initialized. To create a snapshot of the files and folders changed in a local repository `git commit` command can be used.
- Remote repository: The purpose of a remote repository is sharing the code with multiple people. It is simply a copy of the versioning data on a remote machine. Files can be added or changed in this repository using `git push` from the local repository and changes can be taken using `git pull` to local repository.


### Creating a local repository
Git is used to track changes made to a project's files. It needs to be initialized onto a project to create a git repository.
```
git init
```
![n5Vt1RG5Eh](https://user-images.githubusercontent.com/48220015/111876093-27348400-89ae-11eb-83d9-f8b01cdae9b1.gif)

> Initializing a git repository will create the folder `.git` in the project's location. It stores the history of all changes made to files in the project. Simply means that deleting this folder is also deleting the project's history.

After creating a repository, project files can be changed, and commits can be made.
```
git add . 
git commit -m "Initial commit"
```
![zuLxHin4lz](https://user-images.githubusercontent.com/48220015/111876376-78914300-89af-11eb-8a25-6f0bddff2060.gif)


### Adding an existing local repository to SourceTree
An existing local repository can be added to SourceTree environment.<br/><br/>
![dxaFmB3ynU](https://user-images.githubusercontent.com/48220015/111876412-b2fae000-89af-11eb-93ee-aa6da67380b4.gif)


### Cloning a remote repository
Cloning a repository creates a fully copy of the repository data for that specific time to the local machine. It will copy every file and folder on that project including their all versions.

A repository can be cloned from GitHub to a local machine using HTTPS or using an SSH key.<br/>
Those can be found in the main page of the repository.<br/><br/>
![5UJdCVDURA](https://user-images.githubusercontent.com/48220015/111876503-11c05980-89b0-11eb-84ea-7737023bc715.gif)

Using the copied URL, repository can be cloned to the local machine.
```
git clone <repo>
```
![XqXZ4UOvDD](https://user-images.githubusercontent.com/48220015/111876557-50561400-89b0-11eb-9286-1ed8dc31f52f.gif)

Then it is possible to push changes to the remote repository on GitHub or pull others' changes from GitHub.
```
git add .
git commit -m message
git push
```
![cMTWgHpTfP](https://user-images.githubusercontent.com/48220015/111876737-25b88b00-89b1-11eb-8b49-7825169a066f.gif)

<p align="right"><a href="../README.md#contents">Go back</a></p>
