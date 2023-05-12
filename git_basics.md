# Git Basics

## Uploading file from local machine to Github

1. step 1:
Initialize git in the local repo

```
git init
```

2. step 2:
add the files. Using '.' will upload everything in the repo.

```
git add <filel name> or <.>
```

3. step 3:
Commit the changes

```
git commit -m 'message'
```

to do adding and committing at the same time (not recommended). Only works for modified parts not the newly created ones.

```
git commit -am 'message'
```

4. step 4:
create an empty repo and copy SSH --> This is step is to connect the local repo to remote repo

```
git remote add origin <SSH>
```

USing following command wil show any remote repo that is connected to the local repo

```
git remote -v
```

5. step 5:
now push changes from the local repo to the remote repo 

-- -u is used to indicate up stream

```
git push -u origin master
```

## Branching 

Branches are:
* master branch 
* feature branch --> adding new features and development
* hot fix branch --> fixing major bugs

At first, feature branch and master branch are the same. Then we start adding changes over the feature branch. Each brnahc is only tracking what changes are made in its own branch. It can't get info from the other branches.


#### get current branch
To know the current branch --> * means I am currenly in that branch

```
git branch
```

#### create a new branch

``` 
git checkout -b <branch_name>
```

#### to switch between branches


```
git checkout <branch name>
```

#### Pull Request (PR)
means to have your code on another branch. e.x., we have the feature branch and we want to pull them to the main branch.

When we make a PR from the feature branch to the master branch, every one can do:
* review the code
* comment on it
* ask to make changes


#### getting changes from remote to local repo

```
git pull
```

#### Deleting a branch
After merging the branch to the main branch, we need to delete the branch

This command is used for deleting local branches that are already merged.

```
git branch -d <branch name>
```

#### merge conflicts
In some cases, there will be conflict between the changes in the feature branch and the main branch. When merging 2 branches and this conflict exists, the conflict error will show and and you need to manually fix the issue in your code editor, etc. 


#### Undoing mistakes
after adding using 

```
git add 
```

You can unstage changes by using 

```
git reset <file name>
```

to undo a commit, the following command is used.

```
git reset HEAD~1
```

HEAD --> means a pointer heading to the last commit. 

HEAD~1 --> this will move one step further and put the head to the previous commit. 

Git commits are differentiated by their hashes and they can be accessed using 

```
git log
```

if you want to undo a certain commit back in time, you need to get the hash of that commit and then use

```
git reset <commit-hash>
```

To undo several commits and removing them you do the following.

```
git reset --hard <commit-hash>
```
it will remove all the commits after the hash provided infront of it.


#### Forking

It will make a full copy of a repo. You do not fork your own repo as you have access to all the code there! but you do not have access to other people repos. So you need to fork on their repo!

After forking a repo, you now have full access to everything. Bring it down to your local machine and start doing changes and then ask for PR to the main repo.






























































