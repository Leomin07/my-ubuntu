### Dump setting extensions
 - Dump
```
dconf dump /org/gnome/shell/extensions/ > dump_extensions.txt
```
 - Load file
```
dconf load /org/gnome/shell/extensions/ < dump_extensions.txt
```

### Export Installed Extensions
```
gnome-extensions list --enabled > extensions.txt
```
### Reinstall Extensions Later
```
while read -r uuid; do
    gnome-extensions enable "$uuid"
done < extensions.txt
```

### Virtual Machine Manager

```
sudo apt install ssh-askpass virt-manager
```
