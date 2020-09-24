---
layout: post
title:  "GIT helpful commands"
date:   2020-09-25 01:40:00 +0530
categories: general 
---

# Simple GIT Startup Guide for Beginners

Prequistes
1. Register & create a github account
2. Install git cli on system [apt-get install git]


Commands we shall try are :
```
git init    //Initialze Local git repo
git config --global user.name "HardY"  // Before working on git repo we define user
git config --global user.email "your_email@gmail.com"  // Befor working we define git user email
git status  //Check status of working tree
git add     //Add files to Index in staging stage
git rm --cached  //Remove files from Index in staging stage
git commit -m "Message" //Commit changes in Index in local_repo
git push  //Push to remote repo
git pull  //Pull latest from remote repository
git clone //Clone repository into a new directory
git remote add origin <URL> //Define Remote Repository as origin
git push -u origin master // Upload master branch to Remote Repo
git push origin my-new-branch  // Upload local working branch to remote repo
git log // View Logs
````


##### 1. Command to bring a folder into version control (vc). CD into the folder and enter below command
`git init`

e.g. :
```
mkdir test
cd test
git init
```

The above example shall bring "test" folder under git version control (vc)

##### 2. Check the status
`git status`

Understanding vc :
Git init --> Write_code in local_repo ---> Add file to staging env  ---> Commit changes to Local_Repository ---> Push changes to Remote_Repository (Github) 

##### 3. After a folder gets under git vc, we add a file or create a sub folder and add our project 
`git add <file_name>`

e.g.:
```
touch test.txt
git status 
git add test.txt    ----> this adds file to staging env
```
Check the status
`git status`

Removing files from staging
`git rm --cached <file_name>`

##### 4. Next step is to commit into local_repo
Before commit few there are some global configs
```
git config --global user.email "your_email@gmail.com"
git config --global user.name "HardY"
git commit -m "Initial commit"
```
##### 5. Concept of master , branching , merging

Lets suppose in inception phase of a project , Project manager creates a stickman layout. Stores this in Inhouse Private Git repo. He assigns task to team members and each team member works on local code copy by first branching. after review and completion of task developer request to merge  

On developer machine:
```
git status   -----> This will show status and current branch on which developer is working. Git pull could be used to download master branch
git branch <name_of_the_branch>   ----> create a new branch from master branch
git checkout <name_of_the_branch>  ----> Start working on the branch
git add <files_that_were_added>   ---->Deceloper works on tasks and completes and add it to staging
git commit <files_that_were_created>  -----> Commits the files to local branch  

git checkout master
git merge <name_of_the_branch>
```
On manager
```
git checkout master
git merger  
```

##### 6. Git Push to remote repository
```
git remote add origin <URL_to_your_repo>
git push -u origin master
git push origin my-new-branch
````

##### 7. View Git Logs
```
git log
```