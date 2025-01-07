# Lets look at git locally first

## To start create a new repo

```
mkdir git_demo_1
cd git_demo_1
git init
git status
```

## Now lets add a file
```
echo "This is a git demo" > README.md
git status
git add README.md
git status
git commit -m "first commit"
git status
```

## Create a branch
```
git checkout -b 'new_branch'
git status
cat README.MD
```
## Invistigate how the branch impacts changes
```
echo "This demo is fun" >> README.md
cat README.MD
git status
git add README.md
git commit -m 'second commit'
cat README.MD
```

What does it look like on master?

```
git checkout master
git log
git status
cat README.md
```

What if we want those changes we made on the branch?

```
git merge new_branch
git status
git log
cat README.md
```

```
echo "Lets make another commit" >> README.md 
git add README.md 
git commit -m 'third commit'
git status
git log
```

## What about tags

Lets tag that branch

```
git tag release_1 <commit>
git log
```

Lets go to the tag... read git's output carefully
```
git checkout release_1
cat README.md
```

How do we get back to master?
```
git checkout master
```

