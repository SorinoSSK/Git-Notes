# Git Notes

## Workflow
Edit -> Add -> Commit -> Push

## Syntax
### .
**.** represents all/everything

## restore
Restore all modified code in your local file to initial. Restore function will not restore newly added files.
```
git restore .
```

## add
Add creates a checkpoint of items modified in your local file. 
```
git add .
```

## commit
Commit sets the closure for the list of checkpoint (add) made in your local file.  
You may or may not fill in (Your message). (Your message) will serve as a description for your modification.
```
git commit -m "(Your message)"
```
### modifying commit message
You can modify the message of your last commit
```
git commit --amend
```
To save and quit the edit interface use the following command
```
:wq
```

## branch
### creating branch
Branch can be created on github webpage or on the command prompt. (BranchName) can be any unique name. Always ensure to check that your are on master before creating branch using ```git branch```.
```
git checkout -b branch-(BranchName)
```
### changing branch
You can change your working branch to another branch.
```
git checkout branch-(BranchName)
```
Master is considered a branch.
```
git checkout master
```

## status
Status allows you to track changes made in your file.  
Red coded lines represents files that have not been added for push.  
Green coded lines represents files that have been added for push.
```
git status
```

## push
### push changes to github on undefined branch
Creating a branch on your local terminal will create a branch on your local respository but not on github. (BranchName) is the name of the newly created branch. 
```
git push -u origin branch-(BranchName)
```
### push changes to existing branch
```
git push
```

## pull
### Pull from other branch and overwrite current branch.
Overwrite all files of current branch with the intended branch.
```
git pull origin (BranchName)
```

## delete
### delete a branch
User must not be in the branch it is deleting. If changes have been made, you have to commit before changing branch and deleting it.
```
git branch --delete (BranchName)
git branch -D (BranchName)
```

## update local file
```
git fetch --all
git reset --hard origin/master
```

## code
You may use the following command to access your project file on the selected branch in visual studio.
```
code .
```
## Link git repository to a folder.
```
git clone (copy command from repository).
```
