# **git clone <SSH ID>**         
    # pulls your github project to the local directory

# **git config --global user.email "you@example.com"**     
    # self explanotrii

# **git config --global user.name "Your Name"**
    # self explanotrii

# **cd GitHub**                  
    # change directory to "\GitHub"

# **cd demo1**                   
    # change directory to "GitHub\demo1"

# **git status**                 
    # shows current status of your repo, whether its up to date with the local file or not
        __![alt text](image.png)__
    # "modified" : existing file will have some changed that are not tracked

# **git add .**                  
    # tracks all the changes made ("." represents ALL files u want to track), can also mention specific file names
        __![alt text](image-1.png)__

# **git commit -m "pls work"**   
    # uploads your edited repo locally; "-m" represents a MANDATORY-to-insert message, use it to tell why the  change was made, this is shown as TITLE on your GH

# **git commit -m "pls work" -m "this is an edit"**
    # the second "-m" adds actual description to the change in GH 
        __![alt text](image-2.png)__

# **git push**
    # actually pushes and uploads your file to GH account
        __![alt text](image-3.png)__

# **cd ..**
    # to roll back to the previous folder

# **git init**
    # initialises an empty Git repository if u make a folder locally then want to push to GH
        __![alt text](image-4.png)__

# **Origin push error**
    # Git is trying to say that the file that has to be pushed to origin can not be found, thats because we made it locally so git has nowhere to show that on GH
        __![alt text](image-5.png)__

# to deal with this you have these options: 
    1. Manually create a new EMPTY repo on GH then do this:
        __![alt text](image-6.png)__

# **git remote add origin <REPO ID>**
    # sets the new empty repo to origin

# **git remote -v**
    # shows all remote repositories linked with the in-use repo

# **git push -u origin master**
    # the "-u" adds an upstream, i.e, it sets "origin master" to the default push place so u dont have to type it again n again after this

# ✨__![alt text](image-7.png)__⭐

# **git branch**
    # checks and tells you what branch you are on, master is the main branch and other branches will be the side branches of the project
        __![alt text](image-8.png)__

# **git checkout -b <BRANCH_NAME>**
    # makes and switches yourself to the new branch
        __![alt text](image-9.png)__

# **git checkout <BRANCH_NAME>**
    # switches you to another branch you want to go to (doesnt make a new one)
        __![alt text](image-10.png)__

# **git diff**
    # shows the differences of changes
        __![alt text](image-11.png)__
        __![alt text](image-12.png)__

# PR = pull request
    # when you push a change from your local machine, it hints you to set up a pull request for that branch on GH by visiting the link, it also provides you the link itself
    __![alt text](image-13.png)__
    __![alt text](image-14.png)__

# The arrow denotes which branch is merged into which branch, so the feature1... branch is being merged into MASTER
    __![alt text](image-15.png)__

# even after this the changes wont be in your local machine until you pull them from GH first

# **git branch -d feature1...**
    # deletes the branch
        __![alt text](image-16.png)__

# **git commit -am**
    # Helps to commit and add message to a modified file, WILL not work for newly created files.

# Merge conflicts
    __![alt text](image-17.png)__
    __![alt text](image-18.png)__

# Now you can either use GitHub to fix the merge conflicts or you can just use the options provided in the code editor

# The top line shows the changes from the branch we are currently on
    __![alt text](image-19.png)__

# The bottom line shows the changes coming from other branches
    __![alt text](image-20.png)__

# Just manually delete the extra lines and make the code how you want it to be
    __![alt text](image-21.png)__

# **git reset**
    # this helps you to UNDO a particular (specify nameof file) or all changes in files.
    __![alt text](image-22.png)__

# **git reset HEAD~n**
    # this helps to unstage a COMMIT entirely
    __![alt text](image-23.png)__

# The *~1* part after the HEAD text shows how many commits u wanna go back. We skip over the commit we accidently made and go back to the previous commit that didnt have any problmes for us.

# **git log**
    # this will show you all the commits that were made to the repo (latest to oldest order) so u can see how many commits u wanna go back

# say u have a beef with the latest commit (__![alt text](image-24.png)__) 

# copy the code for that commit (*980cf5c369231e2a03228fb9cd76430890221a2b*) and use **git reset** *number u copied*

# **git reset --hard <log number>**
    #this will HARD REMOVE all the changes after a certain point not just unstage them