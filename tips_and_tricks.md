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



# Download Fonts 

1. Create a local font directory

```
mkdir -p ~/.local/share/fonts/nerd-fonts
cd ~/.local/share/fonts/nerd-fonts
```

2. Download and extract the latest JetBrains Mono Nerd Font

```
curl -fLO https://github.com/ryanoasis/nerd-fonts/releases/latest/download/JetBrainsMono.tar.xz
tar -xf JetBrainsMono.tar.xz
rm JetBrainsMono.tar.xz
```

3. Rebuild Ubuntu's font cache so all apps can see it

```
fc-cache -fv

```

