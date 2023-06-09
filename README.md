# Git Notes

## Workflow
Edit -> Add -> Commit -> Push

## Syntax
### 1) .
**.** represents all/everything

### 2) restore
Restore all modified code in your local file to initial. Restore function will not restore newly added files.
```
git restore .
```

### 3) add
Add creates a checkpoint of items modified in your local file. 
```
git add .
```

### 4) commit
Commit sets the closure for the list of checkpoint (add) made in your local file.  
You may or may not fill in (Your message). (Your message) will serve as a description for your modification.
```
git commit -m "(Your message)"
```
#### 4.1) modifying commit message
You can modify the message of your last commit
```
git commit --amend
```
To save and quit the edit interface use the following command
```
:wq
```

### 5) branch
#### 5.1) view all local branch
You can view all branches created in your local repository using the following command.  
```
git branch
```
#### 5.2) view all available branch
If a branch to to appear when using the above command, then the branch is not pulled to your local repository. Therefore, to view branches of both local and remote repository, you will use the following command.
```
git branch -r
```
#### 5.3) creating branch
Branch can be created on github webpage or on the command prompt. (BranchName) can be any unique name. Always ensure to check that your are on master before creating branch using ```git branch```.
```
git checkout -b branch-(BranchName)
```
#### 5.4) changing branch
You can change your working branch to another branch.
```
git checkout branch-(BranchName)
```
Master is considered a branch.
```
git checkout master
```

### 6) status
Status allows you to track changes made in your file.  
Red coded lines represents files that have not been added for push.  
Green coded lines represents files that have been added for push.
```
git status
```

### 7) push
#### 7.1) push changes to github on undefined branch
Creating a branch on your local terminal will create a branch on your local respository but not on github. (BranchName) is the name of the newly created branch. 
```
git push -u origin branch-(BranchName)
```
#### 7.2) push changes to existing branch
```
git push
```

### 8) pull
#### 8.1) Pull from other branch and overwrite current branch.
Overwrite all files of current branch with the intended branch.
```
git pull origin (BranchName)
```

### 9) delete
#### 9.1) delete a branch
User must not be in the branch it is deleting. If changes have been made, you have to commit before changing branch and deleting it.
```
git branch --delete (BranchName)
git branch -D (BranchName)
```

### 9.2) reset and update local file
```
git fetch --all
git reset --hard origin/master
```

### 9.3) code
You may use the following command to access your project file on the selected branch in visual studio.
```
code .
```
### 9.4) clone a remote git repository to a folder.
```
git clone (copy command from repository).
```
