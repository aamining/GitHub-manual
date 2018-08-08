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
and follow command . usually need to manually set the conflicts and commit aswell.


# How to back to older version (locally - on computer)

Note: just remember that the newer code will be lost.

If we want to back to older version of our code in computer just:

```
git reset --hard <code verion hash>     

(this 7 digits hash is referred to our code version)

by just git reset --hard we can find the current head.

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