# Question 5 - Storage Assessment

## Command

```bash
lsblk
```
### Purpose
I used this to see the disks and partitions on the system.
### Observation
The output listed block devices and their mount points. I could tell which disks were attached.

## Command

```bash
df -h
```
### Purpose
I checked how much disk space was used and available.
### Observation
The report showed sizes in human-readable form. I could see which filesystems had more free space.

## Command

```bash
df -i
```
### Purpose
I checked inode usage on the mounted filesystems.
### Observation
The output showed how many inodes were used and free. I used it to see if any filesystem was low on inodes.

## Command

```bash
du -sh /etc /var /home
```
### Purpose
I wanted to compare the sizes of common directories.
### Observation
The command printed the total size of each directory. It helped me see which folders used the most space.

## Command

```bash
mount | column -t
```
### Purpose
I listed the mounted filesystems in a cleaner table format.
### Observation
The mount points and device names were easier to read. It showed the filesystem type and options too.

## Command

```bash
findmnt -no TARGET,SOURCE,FSTYPE,OPTIONS /
```
### Purpose
I looked up the root filesystem mount details.
### Observation
The output showed the root mount source and filesystem type. I confirmed the options used for the root mount.
