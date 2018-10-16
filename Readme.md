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

Read the modified Readme.md in login branch for learning branching basics....
<br />
~~Completed Branching Basics~~
<br />
<br />
<br />
<br/>
## Now we'll start working with remote repository, which in our case is located at github.
Created repository in github with name *Basics_of_Git*.
<br />
<br />
Use below commands to connect Your Local Repository To Your GitHub Repository. Having a local repository as well as a remote (online) repository is the best of both worlds. You can tinker all you like without even being connected to the Internet, and at the same time showcase your finished work on GitHub for all to see.<br/><br/>
**git remote add origin ~~https://github.com/confusedAI/Basics_of_Git.git~~**

 * origin is an alias on your system for a particular remote repository.For further info check image on *first_tutorial* folder.

**git push -u origin master**
<br />
<br />
<br/>
### Download or clone whole repository from github:
Go to *clone or download* option. From there you can download repository as zip or copy the link then type command<br/>
**git clone** _~~link-name~~_ --- to download whole repository as a folder, where _~~link-name~~_ is your copied link.
<br />
<br />
Suppose many developers are working on a project and someone made a change then you can use **git pull** to get new changes. In our case it showed *Already up-to-date* because nothing has changed between remote and local repository.
<br />
<br />
<br />
### Revert back to some previous version(or commit)
**git reset --hard ~~SHA value of your version(i.e. value after commit keyword)~~**<br/><br/>
You can get this value by using command: **git log**
<br />
