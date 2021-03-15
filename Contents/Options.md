<p align="right"><a href="../README.md#contents">Go back</a></p>

# Options and Preferences

Some of the options and preferences needs to be set up just after installing the SourceTree such as user information and authentication method. There are also some other options which may be useful.

### Creating an SSH key
SSH keys can be used as an authentication method to [connect to GitHub](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh) remotes and services. SourceTree is using PuTTY to generate the keys.
- In toolbar, under `Tools` menu choose the `Create or Import SSH Keys` options.
- This will open the `PuTTY Key Generator`, click `Generate` to start generating an SSH Key.
- It is expecting you to generate some randomness while creating a key, move the mouse over the blank area continuously until it completes the job.
- Set a password for the key and save both public and private keys to your local machine.
- Before closing the window copy the public key so we can directly use it to add to GitHub.

![cP6mLrYNFP](https://user-images.githubusercontent.com/48220015/111969521-64faef00-8b0b-11eb-9b6a-65f2147f25f6.gif)

### Adding an SSH key to GitHub

- After copying the SSH public key, go to your account `Settings` and click `SSH and GPG keys`.
- From this page, click the `New SSH key` button.
- Enter a title and paste the public key.
- Click `Add SSH key` and finish the process by confirming GitHub your password.

![3IHLZGoTAw2](https://user-images.githubusercontent.com/48220015/111971648-9d033180-8b0d-11eb-98af-6af4b30031b5.gif)

SourceTree is now ready to use this key. `Launch SSH Agent` from `Tools` menu and find your private key location to set this.

![OGi6TUmuU9](https://user-images.githubusercontent.com/48220015/111971937-ed7a8f00-8b0d-11eb-807b-70359e0ce782.gif)

### Other options

Options and Preferences can be found under `Tools -> Options`. Arranging some of these options may be very helpful just after the installation. 

- While [installing the SourceTree](Setup.md#Installing), it was asking for user information to set the git configurations. If it is ever needed to change them, they can be found under `Default user information`.
- Since SSH key is already set up, `SSH Client Configuration` has the location of the SSH Key. If needed it can be changed from here also.
- Repo settings can be arranged to set a project folder. So, SourceTree can use this location to put cloned or created project folders as a default. This option can be very helpful while cloning a project since SourceTree will create the path automatically when you pasted the repository url.

![7wp0xgiYLA](https://user-images.githubusercontent.com/48220015/111972096-1e5ac400-8b0e-11eb-9292-4b51ffcbe50f.gif)

I also recommend enabling the [Force Push](ForcePush.md#force-push-git-push), since it may be required later.<br/><br/>
![zJIng8Ppdg](https://user-images.githubusercontent.com/48220015/111972191-3cc0bf80-8b0e-11eb-8d3a-c65f115a4de4.gif)

<p align="right"><a href="../README.md#contents">Go back</a></p>
