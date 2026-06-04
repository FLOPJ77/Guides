# Tips and Tricks

### tree

Install it:
sudo apt update && sudo apt install tree

```
tree -h --du
```

Only show directories (hide individual files)
```
tree -h --du -d
```

Limit the depth - if you only want to see the top 2 levels of your folder structure:
```
tree -h --du -L 2
```

Sort by size - to see the largest files/folders at the top:
```
tree -h --du --sort=size
```
