**command are in bold**   
*Specific names such as folder name,file name are in italics*


**git init** ---  Creates a *.git* (hidden) folder in our *Basics* folder. We have initialized *Basics* as a git repository and now we can start to
 use git commands.
 <br />
<br />
Now we'll add our name and mail to git ---
**git config --global user.name _confusedAI_**
**git config --global user.email _0shivam33@gmail.com_ **
<br />
<br />
**git add Readme.md** --- adding *Readme.md* to our git repository
<br />
<br />
**git status** --- 

                 Under *changes to be committed:*
                              Files in staging area, waiting to get commit (git will take the snapshot of our repository at the time we commit).

                 Under *untrackd files:*
                              Files to be added to staging area, so that they will be included in what will be committed).

<br />
**git rm --cached Readme.md** --- removes *Readme.md* from the staging area. Now if we do **git status** we*ll see two untracked files.
<br />
**git add *.txt ** --- adds all txt files to the staging area.
<br />
**git add . ** --- adds everything to the staging area.
<br />
<br />
<br />
<br />

**git commit** ---  opens a vim editor to write git commit message(i.e. description about what changes you made, so that when you revert back to this version you can remember exactly with what changes you committed your repository at this version).
<br />
<br />
<br />

**git commit -m  _<commit message>_ ** --- no need to open vim, just give the commit message in place of *<commit message>* within " ".
<br />
<br />



# Let's now see how to use ------------ *.gitignore file*
Add all the names of files, folders, etc in *.gitignore* file, that you don't want in your repository so that even if you type command **git add .**
 all the things in *.gitignore*  will be ignored and won't be added to staging area.
**touch .gitignore**
<br />
I don't want to include folder *dir2* so I added */dir2* in *.gitignore*
<br />
<br />
<br />
# Type **git checkout -b login**  --- Create  branch name *login*  which will be a exact copy of your master branch.
**git checkout login **           ---     Switch to login branch
Read the modified Readme.md for learning branch in login.
<br />
*Completed Branching Basics*
<br />
<br />
<br />
# Now we'll start working with remote repository.
Created repository in github with name *Basics_of_Git*.
We should add README.md describing our repository and use .md(mark down) so that information explaining our repository displays nicely.
<br />
<br />
Use below commands to connect Your Local Repository To Your GitHub Repository. Having a local repository as well as a remote (online) repository is
 the best of both worlds. You can tinker all you like without even being connected to the Internet, and at the same time showcase your finished work
 on GitHub for all to see.
**git remote add origin https://github.com/confusedAI/Basics_of_Git.git**
**git push -u origin master**
<br />
<br />
Download or clone whole repository from github:
Go to *clone or download* option then you can download repository as zip or copy the link then type command
**git clone <link>** to download whole repository as a folder.
<br />
<br />
Suppose many developers are working on a project and someone made a change then you can use **git pull** to get new changes. In our case it showed
 *Already up-to-date* because nothing has changed between remote and local repository.
<br />
<br />
<br />
Revert back to some previous version(or commit)
**git reset --hard <SHAsum of your version(i.e. value after commit keyword)>**
You can get this value by using command **git log**
<br />

