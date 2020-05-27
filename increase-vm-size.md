# XenServer Increase VM Size

## Ubuntu/Linux

### Steps

1. Turn Off VM
2. Select VM
3. Select **Storage** Tab
4. Right click Virtual disk
5. Select **Properties**
6. Select **Size and Location**
7. Increase Size
8. Click **OK**
9. Turn On VM
10. **fdisk -l** to check/see what your drives are
11. **fdisk /dev/xvda** or whatever the virtual disk’s ID is — main disk, not an individual partition
12. **p** - print the partition table, e.g 2
13. **d** then **2** to delete the 2nd partition
14. **n** then **2** to create a new partition over the old one
15. Press **Enter** for first sector and last sector as default
16. **N** to not remove the signature 
17. **w** to write the new partit ion table
18. **resize2fs /dev/xvda2** to re-size the file system to match the partition table for the 2nd partition
19. **df -h** to check Virtual disk updated size
