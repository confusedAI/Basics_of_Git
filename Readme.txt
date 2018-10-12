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



