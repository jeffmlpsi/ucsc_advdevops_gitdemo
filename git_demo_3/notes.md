# Lets checkout a PR so we can test it

Grabbing from a real project ...

```
git clone git@github.com:canonical/lxd.git
```

Find a PR from the UI ...

Lets pull the change down
```
git fetch <remote> pull/$PRNUMBER/head:<localbranchname> 
```

Pull it into your workspace
```
git checkout <localbranchname>
```

