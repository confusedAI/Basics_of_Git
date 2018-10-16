This tutorial is prepared from the following video:
**https://www.youtube.com/watch?v=SWYqp7iY_Tc**

**commands** are in bold other than headers.<br/>
Specific names such as *folder name,file name* are in italics.


### Start with the below command to create your local repository
**git init** ---  Creates a *.git* (hidden) folder in our *Basics* folder. We have initialized *Basics* as a git repository and now we can start to use git commands.
##### The first thing to do is add your name and mail to git.

**git config --global user.name ~~confusedAI~~**<br/>
**git config --global user.email ~~mail_id~~**


We should always add *README.md* describing our repository and the reason behind using .md(mark down) extension so that information explaining our repository displays nicely.  
**git add Readme.md** --- adds *Readme.md* to your git repository.   

~~Please also add log.txt file to learn few other commands. It's has no special use,we are just adding it to experiment with other helpful commands.~~
<br/>
<br/>
**git status** ---

 * Under *changes to be committed* ---
                    Files in staging area, waiting to get commit (git will take the snapshot of our repository at the time we commit).<br/>
 * Under *untracked files* ---
                    Files to be added to staging area, so that they will be included in what will be committed).

<br />

**git rm --cached Readme.md** --- removes *Readme.md* from the staging area. Now if we do **git status** we'll see two untracked files* (Readme.md and log.txt)*.
<br />
<br />
**git add \*.txt** --- adds all txt files to the staging area.
<br />
**git add .** --- adds everything to the staging area.
<br />
<br />
<br />

**git commit** ---  Finally we're committing our changes to local repository. This also opens a vim editor to write commit message(description about what changes you made, so that when you revert back to this version you can remember exactly with what changes you committed your repository at this version).
<br />
<br />
<br />

**git commit -m  ~~commit message~~** --- no need to open vim, just give the commit message in place of ~~commit message~~ within double quotes (" ").
<br />
<br />


## Let's now see how to use ------------ *.gitignore file*
Add all the names of files, folders, etc in *.gitignore* file, that you don't want in your local repository so that even if you type command **git add .** all the things in *.gitignore*  will be ignored and won't be added to staging area.

**touch .gitignore** --- created empty file *.gitignore*
<br />
I don't want to include folder *dir2* so I added */dir2* in *.gitignore*
<br />
<br />
<br />
### Branching, mostly used during projects when many people are collaborating on that particular project.
Whenever we say **git status** till now we get _on branch master_. Suppose a team is working on a project and I am given a task of creating a login screen then I can just create a login(or any other name) branch so that I diverge from the main line of development and continue to do work without messing with that main line.


_To create a new branch and switch to it at the same time, you can run the **git checkout** command with the **-b** switch:_

**git checkout -b login** --- creates  branch name *login*  which will be a exact copy of your master branch, and also switches to that branch (_login_).
#### This is shorthand for:
**git branch login**<br/>
**git checkout login**



**git branch login** ---  creats branch named _login_. But doing only this does not change our branch. We have to use command **git checkout login**  to change our branch to login.<br/>

_Follow the below commands:_<br/>
**touch login.txt** --- adds login.txt in login branch.<br/>
**git commit -m '~~commit message~~'**<br/>
**git checkout master** --- You will notice that _login.txt_ file is not there and even _Readme.md_ file is different, because the modified _Readme.md_ and _login.txt_ were in _login_ branch not _master_ branch, so they are different.


**git merge login** --- giving this command will merge branch _login_  with _master_. I did not type this command because I don't want my _Readme.md_ in _login_ to modify my _Readme.md_ in _master_, so that in future I can understand the difference for understanding branching.


Now to push this branch to remote directory which is aliased by _origin_ , you need to type:<br/>
**git push -u origin login** --- you will get the message: _Branch 'login' set up to track remote branch 'login' from 'origin'._   
