### READ ME

This file will highlight some basic GitHub etiquette, rules and basic instructions.

**Originall written on:** Feb 10, 2023 by Sabrina Fang '23 @github/sbrn8

**Other Contributers:**

**EDITs (Latest) on:** _Add edit dates here_

## Why should I use GitHub

1. **Collaborate**

   If there is an assignment that requires you to work with your peers, you may use GitHub to share your contributions.

2. **Showcase your work**

   By consistently publishing your work to GitHub, you are essentially creating a portfolio of all your projects! Today, most companies (even universities) look into GitHub profiles when searching for new recruits.

3. **Version Control**

   When a group is colloaborating on a project, it become difficult to track changes, when the changes were made, and where they are stored. GitHub takes care of this all by keeping track of all the changes that have been pushed to the repository. Similar to using Google Drive, you can have a version history of your code so that the previous version are not lost with every iteration.

## Setup Instructions

<details><summary>Step 0 - Check if you have Git</summary>
  <p>
  
  * Open Terminal (MacOS) or PowerShell (Windows)
  * Write the following command

```
git --version
```

**If it outputs a version number for your git, it means that you have git on your computer! Otherwise, follow the instructions below to install Git.**

**For MacOS users, it might ask you to download X-Code command line tools, promptly download it to proceed to the next step. While you are waiting for the download, you skip step 1 and proceed to Step 2.0 but make sure to go back to step 1 to download Git.**

 </p>
</details>

<details><summary>Step 1 - Install Git</summary>
  <p>

### Install Git

**Windows Users:**

Please follow this link to download Git on your computer. [Download Git](https://git-scm.com/downloads)

**MacOS USers:**

- If trying $ git --version shows a pop-up window asking you to download xcode command line tools. You would have to install it first to proceed by clicking the ‘install’ button. Or input this command in your terminal:

```
xcode-select --install
```

- Please follow the instructions on this link to download Git on your computer. [Download Git](https://git-scm.com/download/mac)
  </p>
</details>

<details><summary> Step 2.0 - Create GitHub Account</summary>

### Create GitHub Account

Create or login to your GitHub Account [here](https://github.com/login) .

  </p>
</details>

<details><summary>Step 2.1 - Configure Git with GitHub</summary>
  <p>

### Configure Git with GitHub

Instructions reference:

[Setting up Git - The Odin Project](https://www.theodinproject.com/lessons/foundations-setting-up-git)

For Git to work properly, we need to let the Git know who we are so that it can link a local Git user (you) to GitHub. When working on a team, this allows people to see what you have committed and who committed each line of code.

The commands below will configure Git. **_Be sure to enter your own information within those quotation marks!_**

```
git config --global user.name "Your Name"
git config --global user.email "yourname@example.com"
```

GitHub has changed its default branch from **masters** to **main**. Change the default branch for Git using this command:

```
git config --global init.defaultBranch main
```

Set your default branch reconciliation behavior to merging.

```
git config --global pull.rebase false
```

**Optional but helpful commands**

    To enable colorful output with git, type:

```
git config --global color.ui auto
```

**_Verify that things are working properly_**

Enter these commands and verify whether the output matches your name and email address.

```
git config --get user.name
git config --get user.email
```

**_For Mac Users_**

Run these two commands to tell git to ignore .DS_Store files, which are automatically created when you use Finder to look into a folder. .DS_Store files are invisible to the user and hold custom attributes or metadata (like thumbnails) for the folder, and if you don’t configure Git to ignore them, pesky .DS_Store files will show up in your commits.

```
echo .DS_Store >> ~/.gitignore_global
git config --global core.excludesfile ~/.gitignore_global
```

  </p>
</details>

<details><summary>Step 2.2 - Create an SSH Key </summary> 
  <p>
  
### Create an SSH Key

An SSH key is a cryptographically secure identifier. It’s like a really long password used to identify your machine. GitHub uses SSH keys to allow you to upload to your repository without having to type in your username and password every time.

First, we need to see if you have an Ed25519 algorithm SSH key already installed. Type this into the terminal and check the output with the information below:

```
ls ~/.ssh/id_ed25519.pub
```

If a message appears in the console containing the text “No such file or directory”, then you do not yet have an Ed25519 SSH key, and you will need to create one. If no such message has appeared in the console output, you can proceed to step 2.3 .

**_Note:_** The angle brackets (< >) in the code snippet below indicate that you should replace that part of the command with the appropriate information.

```
ssh-keygen -t ed25519 -C <youremail>
# When it prompts you for a location to save the generated key, just push Enter.
# Next, it will ask you for a password; enter one if you wish, but it’s not required.
```

  </p>
</details>

<details><summary>Step 2.3 - Link SSH Key with GitHub </summary>
<p>

### Link SSH Key with GitHub

You need to tell GitHub what your SSH Key is so that you can push your code without typing in a password every time.

- First, you’ll navigate to where GitHub receives our SSH key. Log into GitHub and click on your profile picture in the top right corner. Then, click on **Settings** in the drop-down menu.

* Next, on the left-hand side, click **SSH and GPG keys**. Then, click the green button in the top right corner that says **New SSH Key**. Name your key something that is descriptive enough for you to remember where it came from. Leave this window open while you do the next steps.

  Now you need to copy your public SSH key. To do this, we’re going to use a command called **_cat_** to read the file to the console. (Note that the .pub file extension is important in this case.)

  ```
  cat ~/.ssh/id_ed25519.pub
  ```

  Highlight and copy the output, which starts with ssh-ed25519 and ends with your email address.

Now, go back to GitHub in your browser window and paste the key you copied into the key field. Then, click **Add SSH key**. You’re done! You’ve successfully added your SSH key!

</p>
</details>
  
## Git Work Flow

<details><summary>Create a remote repository on GitHub </summary>
  <p>

### Create a remote repository on GitHub

To put your projects up on GitHub, you will need to create a repository for it to live in.

[GitHub Instructions](https://docs.github.com/en/get-started/quickstart/create-a-repo)

**Note**
You **should not** create a README file if you wish to upload projects from your local computer to GitHub, therefore you should leave it unchecked. You can read more about it under ''.

  </p>

</details>

<details><summary>Clone remote repository to Local Computer</summary>
  <p>

When you create a repository on GitHub, it exists as a remote repository. You can clone your repositories to create a local copy on your computer and sync between the two locations.

When you clone a repository, you are "pulling" a full copy of all the data of the repository that GitHub has. You can clone your own existing repository or clone antoher person's existing repository to contribute to a project.

**The following steps works for both empty repositories and repositories with existing files.**

### Clone a repository

[Instructions](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository)

**Steps**

1. On GitHub, navigate to the main page of the repository.
2. Click the green button **Code**
3. Copy the SSH Key for the repository.
4. Open Terminal
5. Change the current working directory to the location where you want the cloned directory.

   ```
   cd <directory>
   # cd desktop
   ```

6. Type **git clone**, and paste the SSH Key after it. _You might have to right click to access the mouse menu to past_

   ```
   git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY
   ```

7. Press **Enter** to create your local clone.

   ```
   git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY
   > Cloning into `Spoon-Knife`...
   > remote: Counting objects: 10, done.
   > remote: Compressing objects: 100% (8/8), done.
   > remove: Total 10 (delta 1), reused 10 (delta 1)
   > Unpacking objects: 100% (10/10), done.
   ```

  </p>

</details>

<details><summary>Upload local projects to GitHub</summary>
  <p>

### Upload local projects to GitHub

If you have existing source code or repositories stored locally on your computer, you can add them to GitHub by typing commands in a terminal. You can do this by typing Git commands directly.

Reference: [Adding locally hosted code to GitHub - GitHub Docs](https://docs.github.com/en/get-started/importing-your-projects-to-github/importing-source-code-to-github/adding-locally-hosted-code-to-github)

1. Create a new repository if you have not already. _If you have trouble with this, you can refer to the previous steps under this section of "Git Work Flow"_
2. Open Terminal.
3. Change the current working directory to your local project.
4. Use the init command to initialize the local directory as a Git repository. By default, the initial branch is called main.

If you’re using Git 2.28.0 or a later version, you can set the name of the default branch using -b.

```
git init -b main
```

If you’re using Git 2.27.1 or an earlier version, you can set the name of the default branch using this command:

```
git init && git symbolic-ref HEAD refs/heads/main
```

5. Copy the SSH Key from your repository on GitHub.
6. In the terminal, add the SSH Key where your projects will be pushed.

```
git remote add origin <REMOTE_URL>
   # Sets the new remote
git remote -v
   # Verifies the new remote URL
```

7. Add the files in your local directory.

```
git add .
```

8. Commit the files that you've staged in your local repository.

```
git commit -m "First Commit"
```

9. Push the files from your local repository to GitHub

```
git push -u origin main
```

  </p>

</details>

<details><summary>Stage, Commit & Push your changes to GitHub</summary>
  <p>
  
### Stage, Commit & Push your changes to GitHub

When you are ready to push your changes to GitHub, there are a few steps to that you have to complete in order to "push" your changes. Do not worry, these steps and commands become very intuitive once you are used to working with Git and GitHub. The steps are as follow:

- Stage - Staged files are files that are ready to be committed to the repository you are working on. As you are working, you may be adding, editing and removing files. But whenever you hit a milestone or finish a part of the work, it is a good habit to add the files to a Staging Environment.

- Commit - Since we have finished our work, we are ready move from stage to commit for our repo. When we commit, we should always include a message that is clear for both yourself and others to see what has changed and when.

- Push - Pushing your commited changes to your GitHub repository!

Here are all the that you would type in your terminal to complete all of those steps:

**Make sure that you are within the directory of your file that you would like to push**

_Commands that begins with # are comments. Do not type them into your terminal_

```
  # Ideally you should be git pull-ing to ensure the local repo reflects the remote repo before doing these steps
  # Go to topic 'Pull changes to local computer" to learn more about git pull

  # *Optional* Check Git Status - files that are unstaged will be coloured red;
  # files that are staged will be coloured green
git status

  # Add helloWorld.java to the staging environment; replace it with your file name
git add helloWorld.java

  # Add all files that are unstaged
git add .

  # *Optional* Check Git Status - your files should be coloured green as they are staged
git status

  # Commit and add commit message
git commit -m "Modified to print 'hello world!'"

  # Push your files to the default remote named 'origin' and default branch named 'main'
git push origin main
```

#### Stage your changes

Reference: [Git Staging Environment - w3schools](https://www.w3schools.com/git/git_staging_environment.asp?remote=github)

For example, let's say you are done working with _index.html_.

Any unstaged files will appear red when you check the **git status**.

```
git add index.html
```

This file should be Staged and therefore appear green. Let's check the status:

```
git status
```

And it should return:

```
On branch main

No commits yet

Changes to be committed:
(use "git rm --cached ..." to unstage)
new file: index.html
```

#### Commit your changes

Reference: [Git Commit - w3shools](https://www.w3schools.com/git/git_commit.asp?remote=github)

Type the following command to commit ALL the staged files and to write a commit message. _Replace the message within the quotation marks with a message that reflects your own changes_

```
git commit -m "Modified index.html"
```

The **_commit_** command performs a commit, and the **_-m "message"_** adds a message.

#### Push your changes

Reference: [Pushing commits to a remote repository - GitHub Docs](https://docs.github.com/en/get-started/using-git/pushing-commits-to-a-remote-repository)

The git push command takes two arguments:

- A remote name, for example, **origin**
- A branch name, for example, **main**

For example:

```
git push REMOTE-NAME BRANCH-NAME
```

As an example, you usually run **git push origin main** to push your local changes to your online repository.

```
git push origin main
```

  </p>

</details>

<details><summary>Pull changes from remote repo to local computer</summary>

  <p>

### Pull changes from remote repo to local computer

Reference: [Git Pull - GitHub Git Guides](https://github.com/git-guides/git-pull)

If you are know what you are doing, here is the command. But, you should continue reading if you are new to this concept.

```
git pull
```

Git pull updates your current local working branch, and all of the remote tracking branches. You should make it a habit to run git pull right before you push your changes to branches and regularly on the branches (repos) you are working on locally. It is also a good idea to run **git status** before **git pull** to avoid changes to be overwritten during git pull.

Git pull is a combination of **git fetch** + **git merge**. **git fetch** updates the remote tracking branches. **git merge** will update your current branch with any new commits on the remote tracking branch.

Sometimes you might want to use **git fetch**:

- when you are expecting conflicts/failures - you will not have to deal with the conflict right away if you do not **git merge**.
- to update all remote tracking branches before losing network connection

  </p>

</details>

<details><summary>Helpful Terminal Commands</summary>
<p>

### Helpful Terminal Commands

#### Change Directory

This command will change the directory that you’re currently working with in the Terminal in order to execute other commands on a different directory, view the contents of a different directory or open a file in a different directory.

```
  #replace <directory> with the name of the directory; exclude <>
cd <directory>

  #to go to your home directory
cd ~

  #to go to the parent directory of your current directory
cd ..
```

#### Listing all files

Use this command after navigating into a directory using the cd command to view the contents (files and directories) inside of the current directory.

```
ls
```

#### Create a directory

This command will allow you to create a directory (folder) right from the CLI. When you need a place to store new files, just use this command to add a new directory in the current working directory, or specify a full path to the location where you want the new directory to be placed.

```
mkdir newFolder
```

#### Clear terminal screen

```
clear
```

  </p>

</details>

## Git Branches

<details><summary>What are Branches</summary>
  <p>

Reference: [Git Branch - w3schools](https://www.w3schools.com/git/git_branch.asp?remote=github)

In Git, a branch is a new/separate version of the main repository.

Let's say you have a large project, and you need to update the design on it. How would that work without and with Git:

- With a new branch called new-design, edit the code directly without impacting the main branch
- EMERGENCY! There is an unrelated error somewhere else in the project that needs to be fixed ASAP!
- Create a new branch from the main project called small-error-fix
- Fix the unrelated error and merge the small-error-fix branch with the main branch
- You go back to the new-design branch, and finish the work there
- Merge the new-design branch with main (getting alerted to the small error fix that you were missing)

Branches allow you to work on different parts of a project without impacting the main branch. When the work is complete, a branch can be merged with the main project. You can even switch between branches and work on different projects without them interfering with each other.

Branching in Git is very lightweight and fast!

  </p>

</details>

<details><summary>Make a new Branch</summary>
  <p>

Reference: [Git Branch - w3schools](https://www.w3schools.com/git/git_branch.asp?remote=github)

### Make a new Branch

Let's say we are to add some new features to our index.html page. We are working in our local repository, and we do not want to disturb or possibly wreck the main project.

So we create a new branch, called "hello-world-images":

```
git branch hello-world-images
```

Let's confirm that we have created a new branch:

```
git branch
  hello-world-images
* main

```

We can see the new branch with the name "hello-world-images", but the \* beside **main** specifies that we are currently on that branch.

**checkout** is the command used to check out a branch. Moving us from the current branch, to the one specified at the end of the command:

```
git checkout hello-world-images
  # Switched to branch 'hello-world-images'
```

Now we have moved our current workspace from the master branch, to the new branch. You can open your editor, Visual Studio Code, and make some changes.

  </p>

</details>

<details><summary>Stage, Commit, Push changes to a Branch</summary>
  <p>

Reference: [Git Branch - w3schools](https://www.w3schools.com/git/git_branch.asp?remote=github)

### Stage, Commit, Push changes to a Branch

You have made changes to a file and added a new file in the working directory (same directory as the main branch). Now, you want to push your changes to the branch on GitHub. It is similar to the steps that you would follow if you were to push changes to **origin main**.

**Check the status of the current branch:**

```
git status
```

**Git pull**

It is a good habit to pull the latest changes of the remote repo to your local repo before pushing your changes to the remote repo. This can avoid merge conflicts.

```
git pull
```

**Add unstaged files to staging environment:**

```
git add <file name>

  # Or to add all unstaged files to staging environment
git add .
```

**Commit your changes:**

```
git commit -m "modified <file name>"
```

  </p>

</details>

<details><summary>Switching between Branches</summary>
  <p>

### Switching between Branches

Let's say you want to switch to another branch. Whether it is from **main** to another branch, or a branch that you have created to another one. The steps are still the same:

```
git checkout <branch name>
```

For example:

```
git checkout main
```

  </p>

</details>

<details><summary>Merge Branches</summary>
  <p>

Reference: [Git Branch Merge - w3schools](https://www.w3schools.com/git/git_branch_merge.asp?remote=github)

### Merge Branches

You fixed the bugs in your project, and now you are ready to merge it to **main**, which is the _good copy_ of the project.

Here are the steps:

First, you need to checkout to main

```
git checkout main
```

Now, you can merge your changes to **main**. _Remember to replace the brackets with the name of the branch that you would like to merge_

```
git merge <branch name>
```

  </p>
</details>

<details><summary>Delete a Branch</summary>
  <p>

Reference: [Git Branch Merge - w3schools](https://www.w3schools.com/git/git_branch_merge.asp?remote=github)

### Delete a Branch

You fixed your bugs in your project and have merged the changes to main. The branch is no longer needed. You can delete it using this command:

```
git branch -d <branch name>
```

  </p>
</details>

<details><summary></summary>
  <p>

  </p>
</details>
