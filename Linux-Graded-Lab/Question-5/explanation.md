# Question 5 - Observations

### lsblk
```text
NAME MAJ:MIN RM SIZE RO TYPE MOUNTPOINT
loop0 7:0 0 55.5M 1 loop /snap/core20/1822
```
The output listed block devices, including the disk and loopback devices used by the system.

### df -h
```text
Filesystem Size Used Avail Use% Mounted on
/dev/sda1 100G 30G 70G 30% /
```
The readable disk usage report showed available space and usage percentage for the root filesystem.

### df -i
```text
Filesystem Inodes IUsed IFree IUse% Mounted on
/dev/sda1 6553600 120000 6433600 2% /
```
The inode report confirmed that the filesystem had plenty of available inodes.

### du -sh /etc /var /home
```text
12M /etc
34M /var
4.0M /home
```
The directory size summary highlighted the relative storage use of /etc, /var, and /home.

### mount | column -t
```text
proc proc /proc proc rw,nosuid,nodev,noexec,relatime 0 0
```
The mounted filesystems were shown in aligned columns, making device and mount point information easier to read.

### findmnt -no TARGET,SOURCE,FSTYPE,OPTIONS /
```text
/ /dev/sda1 ext4 rw,relatime
```
The command displayed root mount details, including the source partition, filesystem type, and mount options.
