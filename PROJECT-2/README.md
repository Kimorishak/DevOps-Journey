# Project 2

## First step is to make directory using `mkdir DevOps ` then change into the directory using the command `cd DevOps` , then lastly initialize git using the command `git init`.

![Alt text](<mkdir and Git Init.png>)

## Next step is to carry out your first commit, using the following commands.

`touch index.txt` 
### It is used to create a file in the current working directory.
`echo`
### the command is used to write any sentence inside the text file.
`git add`
### the command is use to add your changes to git.
`git commit -m`
### the command is used to commit your changes to git.

![Alt text](<git init, commit.png>)

## Make your first git Branch
Uisng ths command `git checkout -b main`

![Alt text](<Create new branch.png>)

### To list the branches on yor local git repository, use this command
`git branch`

![Alt text](<git branch.png>)

### To change into an existing or old branch use the comand below.
`git checkout <branch-name>`

![Alt text](<change to master.png>)

## Merging a Branch into another Branch
`git merge B`

![Alt text](<merge two branches.png>)

## Deleting a git branch, it can be activated using the command below
`git branch -d <branch_name>`

![Alt text](<Delete branch.png>)

## Pushing your local git Repository to your Remote github Repository
`git remote add origin <link to your github repo>`

![Alt text](<git remote add origin.png>)

## After commiting your changes in your local repo. You push the content to the remote repo using the command below
`git push origin <branch name>`

![Alt text](<git push.png>)

## Cloning Remote Git Repository using the following command
`git clone <link to your remote repository>`

![Alt text](<git clone.png>)
