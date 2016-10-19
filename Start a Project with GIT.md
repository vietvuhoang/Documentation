
# Setup SSH key

### Generate SSH key file

```sh
$ ssh-keygen -t rsa -C "vietvh@vsii.com"
```

There are 2 files generated after above command:

- **private key :** id_rsa

- **public key :** id_rsa.pub

> The private key will be store on your workspace PC, and the public ket will be setup on your GIT account

### Setup private key on local 

For setting up the private key, you need copy it into your $HOME/.ssh folder and give it 400 permission

```sh
$ cp id_rsa /home/vietvh/.ssh
$ chmod 400 /home/vietvh/.ssh
```

### Setup publickey on GIT System 

Now, you should copy the content of your public file into your [GIT Account](https://github.com/settings/keys)

```sh
$ cat id_rsa.pub
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDeg7bxNrQhs7gpP68aTe/3AXOgMsF4Z5b+0gpGdS6jDh7vKfEL3z3kozayqEiTJrswJ6yWx+rlrQlu0EoHc2GO6kM+rNKftOINTpGNF2dr4HpHdzGHDf/F02EumNBKgyOlBPokl2IrqWEPINBEMP5wkMin1pc2EzXcqGfKcNDcerWDD1/0xCV8BzcVBDCQCXbmRCUJ2+0Ai4PZmS7ruP2fnWDe16H7igbDoDgobflxKayd2z+2DyFZ5Oar2XkWFGLN6w3vkG9HzhqyKc0Qsi/DL3j4GM5xXtoCsh9Vm8x5bZ0g0sdWScHfSIBpLlH6GeL013eXIwrQO8qCdGczN0ZB vietvh@vsii.com
```

# Clone the Project to local 

Clone project

```sh
$ git clone git@git.vsii.com/YourProject.git
$ cd YourProject
```

# Working with Branches 

In almost case, the default branch you're standing is _develop_. And you must choose your _feature branch_ to start working.

### Check how many branches on your local

```sh
$ git branch
```

### Choose the working branch

If you have the branch already, you choose your branch by following command

```sh
$ git checkout YOUR_BRANCH
```

### Fetch branches to local

In the case you don't have the branch on local yet, you need to fetch it

```sh
$ git fetch
$ git checkout YOUR_BRANCH
$ git pull
```
Now, YOUR_BRANCH is ready on your machine. 
> The **git pull** command helps you pull all updated commits to your local 

### Create new branch on local and push to server
In the case you need your new Branch for working, you could create the Branch and push it to server
```sh
$ git checkout -b NEW_BRANCH
$ git push --set-upstream origin NEWBRANCH
```
### Commit your change
After working in your task, you need to save your changes on a commit. 
First check what you do in this branch
```sh
$ git status
```
Now, stage your files
```sh
$ git add your_awesome_file_1
$ git add your_bullshit_file_2
```
You also could add all change to a commit 
```sh
$ git add .
```
If there is some wrong when you prepare a commit, you could undo it
```sh
$ git reset your_bullshit_file_2
```
And now, when the commit is ready, commit it
```sh
$ git commit -m "What you did on this commit"
```
In the end of work, push all your commits to server
```sh
$ git push
```
### Merge code
When you need your new code from another branch to your working branch, do the merge command
```sh
$ git merge THE_BULL_SHIT_BRANCH_OF_OTHER_GUY
```
> Becareful with is step, there are maybe some conflicts and you must merge code manually.

### The end
Oh, well, now I finish this simple smelling guideline about working with GIT, just have some small remind before finish 
  - You could not push anything before make sure that your changes is the last update
  - You could not swicth to another branch before commiting your changes
  
Now, good luck with GIT

