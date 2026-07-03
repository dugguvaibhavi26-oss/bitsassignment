# Question 5 - Storage Assessment

## Command

```bash
lsblk
```
### Purpose
I listed block devices and their associated partitions.
### Result
The output displayed the storage devices on the machine and the mount points in use.

## Command

```bash
df -h
```
### Purpose
I checked disk usage in a human-readable format.
### Result
The report showed used and available space for mounted filesystems.

## Command

```bash
df -i
```
### Purpose
I checked inode consumption on the system partitions.
### Result
The output showed inode totals and usage percentages, helping identify any inode pressure.

## Command

```bash
du -sh /etc /var /home
```
### Purpose
I compared the total size of common directories.
### Result
The summary showed the storage footprint for /etc, /var, and /home.

## Command

```bash
mount | column -t
```
### Purpose
I displayed mounted filesystems in aligned columns for easier reading.
### Result
The mounted filesystems, devices, and mount options were presented in a clean table.

## Command

```bash
findmnt -no TARGET,SOURCE,FSTYPE,OPTIONS /
```
### Purpose
I inspected the root filesystem mount details directly.
### Result
The command showed the root mount point, source device, filesystem type, and mount options.
