# docker-tools
A collection of scripts that help manage docker

# Tips
See https://medium.com/@porteneuve/mastering-git-subtrees-943d29a798ec

## Adding this repo as a subtree
```
git remote add docker-tools git@github.com:GoBoundless/docker-tools.git
git fetch docker-tools
# you may change "scripts/docker-tools" to be wherever you'd like to save this repo as a subtree
git read-tree --prefix=scripts/docker-tools -u docker-tools/master
```

## Fetching updates from this repo
```
git fetch docker-tools
# you should change "scripts/docker-tools" to be wherever you saved this repo as a subtree
git merge -X subtree=scripts/docker-tools --squash docker-tools/master
git commit -m "Updated docker-tools"
```
