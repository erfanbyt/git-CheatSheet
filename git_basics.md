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
























