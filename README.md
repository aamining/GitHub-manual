# Working with local branches

```
 Git Branch

 - Shows all branches of

 - create a branch with git branch (branch name)

```

```
git checkout

- switch to (checkout) a new branches

- with git checkout (branch name)

```

Example:

1- create a branch called newer ..git branch new

2- switch to new branch .. git checkout new

3- do some changes in code

4- git add --all ( add just changes) and git commit

5- now just switch between 'master' branch and 'new' branch and see two different version of codes

# how to delete a local branch

```
git branch -D <branch name>

```

# merge branches in to master

need to switch to master branch and

```
git merge new master
```
and follow command . usually need to manually set the conflicts and commit as
well.


# How to back to older version (locally - on computer)

Note: just remember that the newer code will be lost.

If we want to back to older version of our code in computer just:

```
git reset --hard <code verion hash>     

(this 7 digits hash is referred to our code version)

by just git reset --hard we can find the current head.

```

# How to back to older version (on github)

```
This line will set the code to the old commit.
git reset --hard <old code version hash or old commit>
```
```
This line set the old commit as the LAST commit and REMOVE the commit(s) after  
git push -f

```


# How to PULL from remote to local from  Github branch -Step By Step

1- Clone repo from remote to local:

```
git clone repoURL

cd to local created directory

```

2- how to checkout to targeted branch

```
git checkout -b xyz           (xyz=brach name)

```
```
git branch --set-upstream-to=origin/xyz
```
you will see this:

```
Branch xyz setup to track remote branch xyz from origin
```
3- git pull

# How to get a repository and all its branches locally

```
mkdir <Folder_name>

cd <Folder_name>

git clone --bare <copy and paste clone link from git hub here> .git

git config --bool core.bare false

git reset --hard

git branch (to see all branches for repo. locally)

git branch <tag> (to switch to other branch)


```
# How to work in other previous commit

```
git checkout <commit tage> (copy commit tag from git)

```
note: After working on other commit,in order to DO NOT  save or commit new
 changes:

```
git stash   (the commit will back to its original and no new commit created)

To Create new commits and push to github we need to be in master branch
So use "git checkout" to see our current branch(head) and git checkout master to
change our head to origin/master. Now we can create new commits and push to
github as new commit.


```
# Create new branch, work on, and merge with origin master

```
create new branch:

git branch<New name>

after working on new branch in order to merge with origin/master branch:

git branch master
git merge <New name>


## do not forget to use "git stash" if do not want to commit new changes or
want to back before any any changes and save or commits
```
