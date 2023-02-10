### READ ME 
This file will highlight some basic GitHub etiquette, rules and basic instructions.

**Originall written on:** Feb 10, 2023 by Sabrina Fang '23 @github/sbrn8

**Other Contributers:** 

**EDITs (Latest) on:** *Add edit dates here*

## Why should I use GitHub
1. **Collaborate** If there is an assignment that requires you to work with your peers, you may use GitHub to share your contributions.
2. **Showcase your work** By consistently publishing your work to GitHub, you are essentially creating a portfolio of all your projects! Today, most companies (even universities) look into GitHub profiles when searching for new recruits. 
3. **Version Control** When a group is colloaborating on a project, it become difficult to track changes, when the changes were made, and where they are stored. GitHub takes care of this all by keeping track of all the changes that have been pushed to the repository. Similar to using Google Drive,  you can have a version history of your code so that the previous version are not lost with every iteration. 

## Instructions
<details><summary>Step 0 - Check if you have Git</summary>
  
  * Open Terminal (MacOS) or PowerShell (Windows)
  * Write the following command

  ```
  $ git --version
  ```
 **If it outputs a version number for your git, it means that you have git on your computer!      Otherwise, follow the instructions below to install Git.** 
  
 ** For MacOS users, it might ask you to download X-Code command line tools, promptly download it to proceed to the next step. While you are waiting for the download, you skip step 1 and proceed to Step 2.0 but make sure to go back to step 1 to download Git ** 
  
 </p>
</details>

<details><summary>Step 1 - Install Git</summary>
  
  ###### Windows Users: 
  
  Please follow this link to download Git on your computer. [Download Git] (https://git-scm.com/downloads)
  
  
  ###### MacOS USers:  
  
  * If trying $ git --version shows a pop-up window asking you to download xcode command line tools. You would have to install it first to proceed by clicking the ‘install’ button. Or input this command in your terminal: 
  ```
  $ xcode-select --install
  ```
  
  * Please follow the instructions on this link to download Git on your computer. [Download Git] (https://git-scm.com/download/mac)
  </p>
</details>

<details><summary> Step 2.0 - Create GitHub Account</summary>
Create or login to your GitHub Account.
  
  [Create a GitHub account](https://github.com/login) 
  </p>
</details>

<details><summary>Step 2.1 - Configure Git with GitHub</summary>
 **Instructions references: [The Odin Project - Setting up Git] (https://www.theodinproject.com/lessons/foundations-setting-up-git)
  
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

<details><summary>Step 2.2 - Configure Git and GitHub </summary>
  

  </p>
</details>
  
