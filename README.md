# Git

## Base `git` commands

#### - `init` create an empty Git repository or reinitialize an existing one

#### - `status` show the working tree status

#### - `diff` show changes between commits, commit and working tree, etc

#### - `add` add file contents to the index

```bash
git add . # add all modified files
git add file1.txt # add only file1.txt
git add my_filder/ # add only files from my_folder
git add -i # add files interactively
```

#### - `log` show commit logs

```bash
git log
git log --online
git log --stat
```

#### - `branch` list, create, or delete branches

```bash
git branch dev # create branch dev
git branch -d dev # delete branch dev
```

#### - `checkout` switch branches or restore working tree files

```bash
git checkout dev # switch to dev branch
git checkout README.dm # restore README.dm file
git checkout f5e4dfb # switch to f5e4dfb commit
git checkout -b dev # create dev branch and switch to it
git checkout f5e4dfb -b backup # create backup branch from f5e4dfb commit and switch to it
```

#### - `reflog` manage reflog information

#### - `commit` record changes to the repository

```bash
git commit -m 'commit message'
git commit -a -m 'commit message' # add all modified files and commit
git commit --amend -m 'new commit message' # edit last commit message
git commit --amend --no-edit # commit files in last commit skipping edit message
```

#### - `cherry-pick` apply the changes introduced by some existing commits

```bash
git cherry-pick f5e4dfb # copy commit f5e4dfb to active branch. obs: this command don't delete original commit
```

#### - `reset` reset current HEAD to the specified state, etc

```bash
git reset # revert the index changes for all files
git reset README.md # revert the index changes for README.md files

# reset (delete) all commits before f5e4dfb
git reset --soft f5e4dfb # does not touch the index file or the working tree
git reset f5e4dfb # --mixed resets the index but not the working tree
git reset --hard f5e4dfb # resets the index and working tree
git reset [ --soft | --hard ] [ HEAD^ | HEAD~1 ] # reset (delete) head commit
git reset [ --soft | --hard ] HEAD~3 # reset (delete) the last 3 commits
```

#### - `restore` restore working tree files

```bash
git restore . # to restore all working tree files
git restore hello.txt # to discard hello.txt changes in working directory
git restore --staged hello.txt # to unstage hello.txt from index
```
