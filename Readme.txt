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



Type "git checkout login" for reading Readme.txt and learning branching.
Completed Branching Basics



Now we'll start working with remote repository.
Created repository in github with name 'Basics_of_Git'.
We should add README.md describing our repository and use .md(mark down) so that information explaining our repository displays nicely.

Use below commands to connect Your Local Repository To Your GitHub Repository.Having a local repository as well as a remote (online) repository is the best of both worlds. You can tinker all you like without even being connected to the Internet, and at the same time showcase your finished work on GitHub for all to see.
"git remote add origin https://github.com/confusedAI/Basics_of_Git.git"
"git push -u origin master"


Download or clone whole repository from github:
Go to 'clone or download' option then you can download repository as zip or copy the link then type command
"git clone <link>" to download whole repository as a folder.
