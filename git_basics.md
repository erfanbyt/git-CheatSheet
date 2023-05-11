# Git Basics

### Uploading file from local machine to Github

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
