# GitHub Tutorial

_by Melanie Paredes_

---
## Git vs. GitHub
* **Git** keeps "snapshots" of code (would keep it saved on a single computer/hard drive)
* In **GitHub** you can store code in the cloud (stored in GitHub which you can access from any computer), keep track of changes and collaborate with others on files
* Git does not need GitHub but GitHub needs Git in order to work 


---
## Initial Setup (making a github account, SSH key)
###### Start by making your own gitHub account. 
1. Go to www.github.com 
2. Make your username your hstat gmail with out the @hstat.org at the end. 


---
## Repository Setup (`init`, your first `add` & `commit`, new repo on github, remote)
###### You can create your own blank directoey of start from someone else's directory. 
1. Make sure you are in `~/workspace/`
2. To make your own blank directory type `git mkdir name-of-directory` Now you should have a green folder to your left with the name you gave it.
3. `cd` into your new directory, do this by typing `cd name-of-directory`. You can also use `cd` to move out of your directory into a parent directory (a level above) by typing `cd ..`
4. Type `git init` in order to initialize git (this is like hiring a family photographer). This is when the directory becomes a repositor.
5. Create a new file by typing `touch file.txt` you should now see a text file under the green folder.
6. c9 into this file and make changes by typing `c9 filename` and typing into the text file.
6. Add this file to the "stage/picture" by typing `git add file.txt`
7. Now you can take a "picture/snapshot" of the people/file on stage by typing `git commit -m "message"` The message should be short and in present tense, this should say what changes you have made that you are taking a picture/snapshot of. 
8. 


---
## Workflow & Commands (status, add, commit, push)
1. `git init`
2. `git status`
3. Add this file to the "stage/picture" by typing `git add file.txt` or `git add .` this will add all the files that are in the current working repository. `git add --all` will add **all** changes including deleted and renamed files.
4. `git status`
5. `git commit -m "message"`
6. repeat 


---
## Rolling Back Changes(undo edit/add/commit/push)
* If you have initialized git in the wrong folder and see (master) you can just unitialize git by typing `rm -rf git`. You should no longer see (master)
* To undo edit 