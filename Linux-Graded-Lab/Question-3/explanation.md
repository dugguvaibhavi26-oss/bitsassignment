# Question 3 - Observations

### ls -li sample.txt hardlink.txt symlink.txt
```text
123456 -rw-r--r-- 2 student student 42 Jul  2 10:45 hardlink.txt
123456 -rw-r--r-- 2 student student 42 Jul  2 10:45 sample.txt
123457 lrwxrwxrwx 1 student student 10 Jul  2 10:45 symlink.txt -> sample.txt
```
The hard link shared the same inode as the original file. The symlink had its own inode and showed the target path.

### stat sample.txt hardlink.txt symlink.txt
```text
File: sample.txt
Size: 42 bytes
Inode: 123456
```
The metadata confirmed the file size and inode values. It also showed the symlink pointing to the original file.

### cat hardlink.txt
```text
Sample content for link analysis
```
I read the hard link and it still showed the sample text. It proved the hard link works even after removing the original name.

### cat symlink.txt
```text
cat: symlink.txt: No such file or directory
```
The symlink failed after deleting sample.txt. That showed the symlink broke because its target was no longer there.
