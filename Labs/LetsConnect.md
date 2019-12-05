# Let's Connect!  
Now that you have Git installed and configured and created a GitHub account, make sure you can pull and push 
to GitHub from your computer. 
**IMPORTANT** You will be cloning repositories down to your local computer. For good organization and accessiblity, create a top
level directory on your laptop now. Call it DCS210 so that you will be able to easily locate your projects.
    
## Overview
* Create a local repository of files using the command line and push it to your GitHub account
* Create a repository in your GitHub account and clone it down to your local machine

### Exercise 1: Create your first repo
#### Create a directory

Navigate to your DCS210 directory

	cd /yourpathto/DCS210
	mkdir my-first-repo
	cd my-first-repo
	
Create a simple text file and spool it out to the terminal:

	echo "Welcome to My First Repo" > readme.txt
	tail readme.txt

Use git to create a local repo. If you want to dive deeper you can read [Getting Started with Git](https://seankross.com/the-unix-workbench/git-and-github.html#getting-started-with-git)  for more details

	git init
	ls -a
What's new in your directory? To turn a typical directory into a repository there must be a .git file in the directory. 
Now we can take steps to __'stage'__ and __'commit'__ changes to files in our reppo. 


	git status
	git add -A
	git status
	git commit -m  "this is my first commit"
	git status

### Questions:

git status will tell you important information about the state of the files in your repo:	
1. Before the 'git add' what did git tell you about the file readme.txt? 
2. After the 'git add' what did git tell you about the file readme.txt?
3. And after the git commit?
4. So what is the difference between a tracked and untracked file?
5. What is the importance of the -m option on the git commit command?
6. How can you remove a file from stage? (Hint: git told you on the command line after the git add command)
7. What happens if you try to use git add when there are no changes to any files?

Now log in to your GitHub account. Why do you __not__ see a repository named 'my-first-repo'
	
### Exercise 2: Using GitHub to create a remote repo
In this exercise we will connect our local repo with our remote repo in our GitHub account.

#### Follow the instructions [Getting Started with GitHub](https://seankross.com/the-unix-workbench/git-and-github.html#github) 

#### Points to Ponder along the way
* When you create a new reposiorty:
	* should you choose public vs. private?
	* should you choose 'initialize with README'?
	* should you add .gitignore?

After you have ![](../images/greenCreateRepo.JPG) you are presented with some options for connecting your 
local and remote repositories. 
* Quick setup - use the https URL with git clone if you have not yet set up a local repo (more on this later)
* ... push an existing repo - since we have already created the local repo

__Getting Connected!__ 

Back in your Anaconda Prompt window in your my-first-repo directory, do the following:
 

	git remote
Nothing is printed because we have not yet connected our local repo to the remote repo. Now connect ...

	git remote add origin https://github.com/yourusername/my-first-repo.git 
	git push -u origin master 

We added a remote named 'origin' to our local repo; the origin's address is the URL

### Questions
1. What does the -u flag do? (Hint: use the man page to find out `git push --help` if this makes no sense google it!)
2. Do you have to use this flag on subsequent push commands?
3. To what do the names origin and master refer? (Hint: google 'what is origin in git' and look for stackoverflow!)
3. How would you modify your local repo and submit the changes to your remote repo (aka GitHub account)
4. If you create a remote repo without having first created a local repo, how would you connect your remote to a local repo?
5. Bonus question: What do you think will happen if you type git push -u instructor master? Why?
 

### Summary of basic git commands used 

| Command         | Notes |
| --------------- | ------ |
|git status| your best friend! use it often|
|git init| start tracking files with git|
|git add | staging|
|git commit | aka 'logging your changes'; aka 'creating a milestone'|
|git add -A | track all of the files in our directory |
|git help 'git command'| e.g., git help status; find out all you need to know about the command|
|git rm --cached filename| command to remove a file from stage __before__ a commit|
|git remote|  |
|remote add origin url | url = address of your repo in GitHub; adds a new remote named 'origin' to your __local__ repo |
|git push -u origin master | initial setup of remote; -u sets origin as the default remote repository|


### Exercise 3 Accept Assignment (includes cloning exercise)