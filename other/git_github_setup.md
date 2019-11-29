# Git Configuration and Github Setup

**IMPORTANT: We will be using Github Classroom for assignment submission. It is important this be setup correctly and that you are comfortable with the 
concept of a repository**

## What is Git?
Git is an open-source version control system and collaboration tool. It is a command line tool which allows
you to track versions of any code or plain text documents that you create. Git organizes groups of files that
you are working with into **repositoriss** which is jsut a directory where all the changes to files in that
directory are tracked.

Check out the [Getting Started](https://git-scm.com/book/en/v2) section of the documentation for 
a more elaborate description. For this class we will only touch on  very basic git comamands for sharing code 
and homework submission.  

## What is GitHub?
Well the authoritative answer is [here](https://git-scm.com/book/en/v2/GitHub-Account-Setup-and-Configuration). But basically it is a Web-based graphical interface for 
interacting with Git. GitHub is a Git repository hosting service (i.e it provides access to remote Git repositories), 
but adds many of its own features. The flagship functionality of GitHub is "forking" - copying a repository
from one user's account to another. This is the main feature we will be using to share class notes and assignments with you. 

Repositories can be public or private. **For this class, all repositories will be private** to ...
 

## What is GitHub Classroom?
GitHub Classroom is a teacher-facing tool that supports the 'forking' of repositories to students in the classroom. 
**All repos are private**
From the student perspective, it facilitates the ...

## Steps for Getting Setup with GitHub

**1. Get Your GitHub Account**
* You will need to register for a github account if you don't already have one
* We recommend using a username that incorporates our name
* . Visit https://github.com, choose a user name that isn’t already taken, provide an email address and a password, 
and click the big green “Sign up for GitHub” button. 

**2. Installing Git**
* You should already have git installed from the Anaconda installation.

**3. Setup options in Git**
* Open a command line application:
    * For Windows, we recommend [Git Bash](http://git-scm.com/download/win) instead of Git Shell (which uses Powershell).
    * For Mac, you will probably be using Terminal, or another command line tool of your choice.
    * Or Anaconda prompt??


	**a. Configure your global git user name and email settings**
	 1. Type `git config --list` to see your current git configuration settings. What is the `user.name` setting? What is the `user.email` setting? Next, we will configure git to use your github user name and email address.
    2. Type `git config --global user.name "YourFirstName YourLastName"` (including the quotes)
    3. Type `git config --global user.email "youremail@domain.com"` (use the email address associated with your GitHub account)
    4. Type `git config --list` again. Those setting should be updated to match the config changes you just made. Note that you can also check an specific setting by typing `git config --global` with no argument.
  
	**b. Generate a SSH key so you don't need to enter your pwd every time you interact with GitHub**
  1. First check to see if you have an SSH key. Complete [this page](https://help.github.com/en/github/authenticating-to-github/checking-for-existing-ssh-keys)
  2. Follow these instructions to ensure you can connect to GitHub from your computer
  
## Let's Connect!  
Now that you have Git installed and configured and created a GitHub account, make sure you can pull and push 
to GitHub from your computer. 
**IMPORTANT** You will be cloning repositories down to your local computer. For good organization and accessiblity, create a top
level directory on your laptop now. Call it DCS210 so that you will be able to easily locate your projects.
    
### Exercise 1: Create your first repo
Assumed Knowledge: create a directory, edit a file, basic shell commands
#### Create a directory

Navigate to your DCS210 directory

	cd /yourpathto/DCS210
	mkdir my-first-repo
Create a simple text file:

	echo "Welcome to My First Repo" > readme.txt

#### Using git to create a local repo [Getting Started with Git](https://seankross.com/the-unix-workbench/git-and-github.html#getting-started-with-git)  

	git init
	git status
	git add 
	git status
	git commit -m  "this is my first commit"
	git status
	
#### Summary of basic commands used 

| Command         | Notes |
| --------------- | ------ |
|git init| start tracking files with git|
|git add | staging|
|git commit | aka 'logging your changes'; aka 'creating a milestone'|
|git add -A = | track all of the files in our directory |
|git help 'git command'| e.g., git help status; find out all you need to know about the command|
|git rm --cached filename| command to remove a file from stage __before__ a commit|


### Questions:
1. What is the difference between a tracked and untracked file?
2. What is the importance of the -m option on teh git commit command?


### Exercise 2: Using GitHub to create a remote repo
To get started, sign in to your GitHub acccount with the credentials you setup earlier

__Note__ that you have a *local* git repository in your DCS210 folder; why is there not a repository named my_first_repo in your GitHub account?

#### Follow the instructions [Getting Started with GitHub](https://seankross.com/the-unix-workbench/git-and-github.html#github) 


#### Points to Ponder along the way
* create repo
	* public vs. private
	* initialize with README
	* add .gitignore
* GitHub suggestions
	* Quick setup = clone
	* the 'remote' = 'origin'

__Getting Connected!__ - In terminal or gitBash, navigate to your DCS directory

	git remote
	git remote add origin https://github.com/yourusername/my-first-repo.git 
	git push -u origin master 



#### Summary of basic commands used 

| Command         | Notes |
| --------------- | ------ |
|git remote|  |
|remote add origin url | url = address of your repo in GitHub; adds a new remote named 'origin' to your __local__ repo |
|git push -u origin master | initial setup of remote; -u sets origin as the default remote repository|

### Questions
1. Look back at your web page for your repository on GitHub (you may need to refresh the page); do you see anything different?
2. To what do the names origin and master refer?

![This is an image](./images/createRepo.jpg)
