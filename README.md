# GitNotes


1. local workspace(working directory)
2. staging
3. local repository
4. remote repository

### Basic

- `git init`
- `git add --a`
- `git commit -m “<commitmessage>”`
- `git push origin <remotebranchname>`
- `git remote add origin <https://....git>`
- `git ls-files`
- `git show <FullcommitId>`
- `git config —global alias.<variableName> “<command except git>”`



### rollback in local workspace(working directory)

- `git restore <fileName>`
- `git checkout -- <fileName>`

### rollback in staging

- `git restore --staged <fileName>`

### rename a file
- `git mv <filename> <newfilename>`

### log
- `git log`
- `git log --oneline --graph --decorate`
- `git log <oldCommitid>...<newCommitid>`

### Show diff

- `git diff`						              **1(working directory)-2(staging)**
- `git diff HEAD`							        **1(working directory)-3(local repository)**
- `git diff —staged HEAD`				      **2(staging)-3(local repository)**
- `git diff master origin/master`			**3(local repository)-4(remote repository)**


### rebase

- `git rebase -i development`
- `git push --force-with-lease`

### reset
- `git reset --hard origin/main`     **Useful in the fork repo after we sync the fork repo's origin/main from original upstream**
- `git reset --hard <oldCommitid>`   **This reset the head and main to the oldCommitid. all the commits above the oldCommitid are discarded (DANGER)**
- `git reset --soft <oldCommitid>`   **This reset the head and main to the oldCommitid. all the commits above the oldCommitid are added in the 2(staging)**
- `git reset --mixed <oldCommitid>`  **This reset the head and main to the oldCommitid. all the commits above the oldCommitid are added in the 1(working directory)**

### config

- `git config --global user.name "your github account username"`
- `git config --global user.email "your github account email"`
