# Question 5 - Observations

### lsblk
```text
NAME MAJ:MIN RM SIZE RO TYPE MOUNTPOINT
loop0 7:0 0 55.5M 1 loop /snap/core20/1822
```
I checked the block devices and saw the system disk plus a loop device. It showed how the storage is laid out.

### df -h
```text
Filesystem Size Used Avail Use% Mounted on
/dev/sda1 100G 30G 70G 30% /
```
Disk usage was shown in readable sizes. I could tell the root filesystem had enough free space.

### df -i
```text
Filesystem Inodes IUsed IFree IUse% Mounted on
/dev/sda1 6553600 120000 6433600 2% /
```
The inode report showed plenty of free entries. It confirmed the system was not running out of inodes.

### du -sh /etc /var /home
```text
12M /etc
34M /var
4.0M /home
```
The directory sizes were summarized clearly. I used this to compare how much space each folder used.

### mount | column -t
```text
proc proc /proc proc rw,nosuid,nodev,noexec,relatime 0 0
```
The mounted filesystem list was easier to read with columns. It showed mount points and options for the active filesystems.

### findmnt -no TARGET,SOURCE,FSTYPE,OPTIONS /
```text
/ /dev/sda1 ext4 rw,relatime
```
The root mount details were shown in one line. I could see the mount source and filesystem type.
