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
$ git --version
```

**If it outputs a version number for your git, it means that you have git on your computer! Otherwise, follow the instructions below to install Git.**

**For MacOS users, it might ask you to download X-Code command line tools, promptly download it to proceed to the next step. While you are waiting for the download, you skip step 1 and proceed to Step 2.0 but make sure to go back to step 1 to download Git.**

 </p>
</details>

<details><summary>Step 1 - Install Git</summary>
  <p>
  
  **Windows Users:** 
  
  Please follow this link to download Git on your computer. [Download Git](https://git-scm.com/downloads)
  
  
  **MacOS USers:**  
  
  * If trying $ git --version shows a pop-up window asking you to download xcode command line tools. You would have to install it first to proceed by clicking the ‘install’ button. Or input this command in your terminal: 
  ```
  $ xcode-select --install
  ```
  
  * Please follow the instructions on this link to download Git on your computer. [Download Git](https://git-scm.com/download/mac)
  </p>
</details>

<details><summary> Step 2.0 - Create GitHub Account</summary>
  
  
  Create or login to your GitHub Account [here](https://github.com/login) .
  
  </p>
</details>

<details><summary>Step 2.1 - Configure Git with GitHub</summary>
  <p>
 Instructions reference: 
 
 [Setting up Git](https://www.theodinproject.com/lessons/foundations-setting-up-git)
  
For Git to work properly, we need to let the Git know who we are so that it can link a local Git user (you) to GitHub. When working on a team, this allows people to see what you have committed and who committed each line of code.
  
  The commands below will configure Git. ***Be sure to enter your own information within those quotation marks!***
  
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
  
  ***Verify that things are working properly***
  
  Enter these commands and verify whether the output matches your name and email address.
  
  ```
  git config --get user.name
  git config --get user.email
  ```
  
  
  ***For Mac Users***

Run these two commands to tell git to ignore .DS_Store files, which are automatically created when you use Finder to look into a folder. .DS_Store files are invisible to the user and hold custom attributes or metadata (like thumbnails) for the folder, and if you don’t configure Git to ignore them, pesky .DS_Store files will show up in your commits.

```
echo .DS_Store >> ~/.gitignore_global
git config --global core.excludesfile ~/.gitignore_global
```

  </p>
</details>

<details><summary>Step 2.2 - Create an SSH Key </summary> 
  <p>
  
An SSH key is a cryptographically secure identifier. It’s like a really long password used to identify your machine. GitHub uses SSH keys to allow you to upload to your repository without having to type in your username and password every time.
  
First, we need to see if you have an Ed25519 algorithm SSH key already installed. Type this into the terminal and check the output with the information below:
  
  ```
  ls ~/.ssh/id_ed25519.pub
  ```
  
  If a message appears in the console containing the text “No such file or directory”, then you do not yet have an Ed25519 SSH key, and you will need to create one. If no such message has appeared in the console output, you can proceed to step 2.3 .
  
  ***Note:*** The angle brackets (< >) in the code snippet below indicate that you should replace that part of the command with the appropriate information. 
  
  ```
  ssh-keygen -t ed25519 -C <youremail>
  # When it prompts you for a location to save the generated key, just push Enter.
  # Next, it will ask you for a password; enter one if you wish, but it’s not required.
  ```
    
  </p>
</details>

<details><summary>Step 2.3 - Link SSH Key with GitHub </summary>
<p>
     
You need to tell GitHub what your SSH Key is so that you can push your code without typing in a password every time.
      
* First, you’ll navigate to where GitHub receives our SSH key. Log into GitHub and click on your profile picture in the top right corner. Then, click on **Settings** in the drop-down menu.

- Next, on the left-hand side, click **SSH and GPG keys**. Then, click the green button in the top right corner that says **New SSH Key**. Name your key something that is descriptive enough for you to remember where it came from. Leave this window open while you do the next steps.

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
To put your projects up on GitHub, you will need to create a repository for it to live in.

[Instructions](https://docs.github.com/en/get-started/quickstart/create-a-repo)

**Note**
You **should not** create a README file if you wish to upload projects from your local computer to GitHub, therefore you should leave it unchecked. You can read more about it under ''.

  </p>

</details>

<details><summary>Clone remote repository to Local Computer</summary>
  <p>
When you create a repository on GitHub, it exists as a remote repository. You can clone your repositories to create a local copy on your computer and sync between the two locations.

When you clone a repository, you are "pulling" a full copy of all the data of the repository that GitHub has. You can clone your own existing repository or clone antoher person's existing repository to contribute to a project.

**The following steps works for both empty repositories and repositories with existing files.**

## Clone a repository

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
   $ git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY
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

  </p>

</details>

<details><summary></summary>
  <p>

  </p>

</details>

<details><summary></summary>
  <p>

  </p>

</details>
