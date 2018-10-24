# GitHub Tutorial

_by Melanie Paredes_

---
## Git vs. GitHub
* **Git** keeps "snapshots" of code (would keep it saved on a single computer/hard drive)
* In **GitHub** you can store code in the cloud (stored in GitHub.com which is a website that you can access from any computer), keep track of changes and collaborate with others on files
* Git does not need GitHub but GitHub needs Git in order to work 


---
## Initial Setup 
##### (making a github account, SSH key)
###### Start by making your own gitHub account. 
1. Go to www.github.com 
2. Make your username your hstat gmail with out the @hstat.org at the end. 
3. On the top right click on the "+" icon and click "New Repository"
![alt text](https://guides.github.com/features/pages/create-new-repo-button.png)
4. Type in repository name under that category, then click on the green box that says "Create repository"
![alt text](https://guides.github.com/activities/hello-world/create-new-repo.png)
5. Now in the blue box there will be a link make sure this link is in SSH key (That means it will only require a one time set up). 
![alt text](file:///Users/a1/Desktop/Screen%20Shot%202018-10-23%20at%208.05.01%20PM.png)
6. Scroll down unitl you see something like this `git remote add origin git@github.com:melaniep7687/trial-run.git` copy and paste this into your c9 (Copy and paste this **only** if the name of your repository in github is the same as the repository in c9 **if not make it the same**)


---
## Repository Setup
##### (`init`, your first `add` & `commit`, new repo on github, remote)
###### You can create your own blank directoey of start from someone else's directory. 
1. Make sure you are in `~/workspace/`
2. To make your own blank directory type `git mkdir name-of-directory` (use the same name you created for your repository in github). Now you should have a green folder to your left with the name you gave it.
3. `cd` into your new directory, do this by typing `cd name-of-directory`. You can also use `cd` to move out of your directory into a parent directory (a level above) by typing `cd ..`
4. Type `git init` in order to initialize git (this is like hiring a family photographer). This is when the directory becomes a repositor.
5. Create a new file by typing `touch file.txt` you should now see a text file under the green folder.
6. c9 into this file and make changes by typing `c9 filename` and typing into the text file.
7. Add this file to the "stage/picture" by typing `git add file.txt`
8. Now you can take a "picture/snapshot" of the people/file on stage by typing `git commit -m "message"` The message should be short and in present tense, this should say what changes you have made that you are taking a picture/snapshot of. 
9. type `git remote add origin URL` the URL should be an SSH link it should be the same thing you copied and pasted before (step 6 of initial setup)
10. Now you can not only save your changes to your local repo (your computer) but to your remote repo (github which is a website you can access from anywhere).


---
## Workflow & Commands 
##### (status, add, commit, push)
1. Initialize git `git init` once you hsve cd into the file you will be working on
2. `git status` This is a very helpful tool becasue it can help you understand what is going on. One example could be when adding files to the stage. When a file has been added or edited but not added to the stage, when you type `git status` it will show up red. Then you can add it to the stage do `git status` and it will show up green. Now it will be ready to be commited.
3. Add this file to the "stage/picture" by typing `git add file.txt` or `git add .` this will add all the files that are in the current working repository. `git add --all` will add **all** changes including deleted and renamed files.
4. type `git status` to see the if its ready to be commited or not. 
5. `git commit -m "message"` This will save your changes to your local repo. A good message should state what you have changed in your file. 
6. repeat these steps to continue commiting files
7. Once you are done or want to save to the remote repo (github) type in `git push -u origin master`, after you have done this once you can just type `git push` and git will know where it will have to push to. 


---
## Rolling Back Changes
##### (undo edit/add/commit/push)
* If you have initialized git in the wrong folder and see (master) you can just unitialize git by typing `rm -rf git`. You should no longer see (master)
* To undo edit you type in `git checkout -- filename` this will undo any changes you have made.
* If you added 2 files to the stage but you only meant to add one you can do `git reset HEAD filename` this will unstage whatever file(s) you just named. 
* To undo a commit type `git reset --soft HEAD~1`
* To undo a commit and unstage the file type `git reset HEAD~1`
* To undo basically everything a commit, add, and edit type `git reset hard HEAD~1`