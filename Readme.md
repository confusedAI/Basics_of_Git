This tutorial is prepared from the following video:
**https://www.youtube.com/watch?v=SWYqp7iY_Tc**

**commands** are in bold other than headers.<br/>
Specific names such as *folder name,file name* are in italics.


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
**git commit -m "~~commit message~~"**<br/>
**git checkout master** --- You will notice that _login.txt_ file is not there and even _Readme.md_ file is different, because the modified _Readme.md_ and _login.txt_ were in _login_ branch not _master_ branch, so they are different.


**git merge login** --- giving this command will merge branch _login_  with _master_. I did not type this command because I don't want my _Readme.md_ in _login_ to modify my _Readme.md_ in _master_, so that in future I can understand the difference for understanding branching.


Now to push this branch to remote directory which is aliased by _origin_ , you need to type:<br/>
**git push -u origin login** --- you will get the message: _Branch 'login' set up to track remote branch 'login' from 'origin'._   
