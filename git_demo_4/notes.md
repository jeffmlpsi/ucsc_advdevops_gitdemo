# How do we update a fork?

## Method 1
So in the UI GitHub provides a 'Sync Fork' button

## Method 2
This isn't strictly required for this operation but there are other uses

First lets checkout our fork
```
git clone git@github.com:drines-uc/lxd.git
cd lxd/
ls
git status
```

We need to add another remote repository
```
git remote -v
git remote add upstream git@github.com:canonical/lxd.git
git remote -v
```

We need to get the updated code from the upstream
```
git fetch upstream 
git status
```

Lets make sure we are on the right branch
```
git checkout master
```

We will now use rebase to rewrite the forks master branch so that our commits are replayed on top of the other branch if they are not already included
```
git rebase upstream/main
git status
```

Nothing left to do but push
```
git push -f origin main
```
