```
              ------------------
              | GIT AND GITHUB |
              ------------------
```
```git status``` :-> gives the status of our project.

```git init``` :-> Initialized empty Git repository.

```git log``` :-> gives commits history.

```git commit -m "message for commit" ```:-> committing in git.

before committing we have to add the project in local repository. by git add <file> or git add *.

if you don't want to do add method then use :- ```git commit -a -m "message"``` this will commit without adding it to local repository.

with command git diff we can check what the new thing is present in the file for committing. if you have add the project to the stage then use git diff --staged to see the difference

for removing from stage use :- ```git rm --cached <filename> ```

```git clone <repository link>``` is used to clone any repository from GitHub to our system.

ls list of all repository, ```ls -a list``` of all hidden repo

for readme use : ```echo "any message">> README.md```

```cat README.md``` :- it is used to read content of the readme

make main branch by :- ```git branch -M main```

```git remote add origin <link>``` :- it is used to connect with GitHub

```git push -u origin main ```:- used to push in GitHub

```git remote -v ```:- gives link from where we fetch and push the request.

Tags are used to mark specific points in Git history as important...

git tag :- gives all the tag that are given till now...

```git tag <tag name> -m "message" ```:- add tag to the repository...
every time we have to push the tag to see changes in the GitHub by:-```git push origin <tag>.```

for branching : git checkout->(old method to branch) and git switch->(new method).
to create branch -> ```git checkout -b <branch name>``` or ```git switch -c <branch name>```

git branch -> gives all the branch in local.
git branch --all -> gives all branches in local or remote.

```git checkout <branch name> or git switch <branch name> : switches between the branch but remember branch should be present for this...```
if you want to go to a previous branch by which you come to that branch then use :-> git switch - 

to delete a branch :-> ```git branch -d <branch name>```

to push a branch :-> ```git push origin <branch name>```

pull :-> ```git pull origin <branch name>``` // if we change in GitHub then we have to do this in order to get the change in local system.

merge two branch :-> 2 ways ->1) by merge 2) by rebase  // for merging we have to in main branch. Always pull before merging
by merge:
	```git merge <branch name>```

by rebase:
	```git rebase <branch name>```

```git stash ```:-> it will save your work without committing . it can be used later by git stash apply

```fork``` -> to copy any other people repository to our repository.


