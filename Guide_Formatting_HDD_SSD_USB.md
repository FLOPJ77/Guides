# Guide_Formatting_HDD_SSD_USB
Basic commands for Linux machines to format Disks

<br>

Check Disk name
```bash
lsblk
```

Check in real time while connecting the disk
```bash
watch lsblk
```

Wiping the Disk writing zeros
> sdX where the "X" stand for the letter of the disk (Ex: sdb)
```bash
sudo dd if=/dev/zero of=/dev/sdX bs=1M status=progress
```

Common block sizes

| Size       | Description |
|------------|-------------|
| `bs=512`   | Small but usefoul for detailed work |
| `bs=1M`    | Standard, works on most disks |
| `bs=4M`    | Fast but some older disks cant handle it |
| `bs=8M`    | Fast sweet spot for HDD |
| `bs=64M`   | For SSD |
| `bs=128M`  | For SSD |

When done, format it
```bash
sudo mkfs.ext4 /dev/sdX
```
<br>

---

<br>


## FAT32 USB drive

Umount

```bash
sudo umount /dev/sdX
```

If umount dosen't work try this

```bash
sudo umount -l /dev/sdX
```

Then format it


```bash
sudo mkfs.vfat -F 32 /dev/sdX
```
