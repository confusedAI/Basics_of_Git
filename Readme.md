"command"


"git init" ---  Creates a '.git' (hidden) folder in our 'Basics' folder. We have initialized 'Basics' as a git repository and now we can start to use git commands.
 

Now we'll add our name and mail to git ---
"git config --global user.name 'confusedAI'"
"git config --global user.email '0shivam33@gmail.com'"


"git add Readme.txt" --- adding Readme.txt to our git repository


"git status" --- 

                 Under changes to be committed:
                              Files in staging area, waiting to get commit (git takes the snapshot of our repository at this time).

                 Under untrackd files:
                              Files to be added to staging area, so that they will be included in what will be committed).


"git rm --cached Readme.txt" --- removes Readme.txt from the staging area.Now if we do "git status" we'll see two untracked files.

"git add *.txt" --- adds all txt files to the staging area.

"git add ." --- adds everything to the staging area.





"git commit" ---  opens a vim editor to write git commit message(i.e. description about what changes you made,so that when you revert to this version you can remember exactly how your repository looked at this version).




"git commit -m  '<commit message>'" --- no need to open vim, just give the commit message between ''.





Let's now see how to use ------------ .gitignore file
Add all the names of files, folders, etc in '.gitignore' file, that you don't want in your repository so that even if you type command "git add ." allthe things in '.gitignore'  will be ignored and won't be added to staging area.
"touch .gitignore"

I don't want to include folder 'dir2' so I added '/dir2' in '.gitignore'
I don't want to include any text file, add '*.txt' in '.gitignore'








Whenever we say "git status" till now we get 'on branch master'. Suppose a team is working on a project and I am given a task of creating a login screen then I can just create a login(or any other name) branch so that I diverge from the main line of development and continue to do work without messing with that main line.

"git branch login" ---  created branch named login. But doing only this does not change our branch. We have to use command
"git checkout login" --- changes our branch to login.
"touch login.txt" --- added login.txt in login branch
"git commit -m '<any message>'"
Now, type "git checkout master". You will notice that login.txt file is not there and even Readme.txt file is different, because the modified Readme.txt and login.txt were in login branch not master branch, So they are different.


"git merge login" --- branch login will be merged with master. I did not type this command because I don't want Readme.txt in master to modify to Readme.txt in login, so that in future I can understand the difference for understanding branching.


Now to push this branch to remote directory, you need to type:
git push -u origin login
you will get the message: Branch 'login' set up to track remote branch 'login' from 'origin'.   
