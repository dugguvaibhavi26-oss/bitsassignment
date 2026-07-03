# Question 3 - Observations

### ls -li sample.txt hardlink.txt symlink.txt
```text
123456 -rw-r--r-- 2 vaibhavi vaibhavi 42 Jul  2 10:45 hardlink.txt
123456 -rw-r--r-- 2 vaibhavi vaibhavi 42 Jul  2 10:45 sample.txt
123457 lrwxrwxrwx 1 vaibhavi vaibhavi 10 Jul  2 10:45 symlink.txt -> sample.txt
```
The hard link shared the same inode number as sample.txt, confirming it references the same data. The symlink had a separate inode and pointed to the original file path.

### stat sample.txt hardlink.txt symlink.txt
```text
File: sample.txt
Size: 42 bytes
Inode: 123456
```
The metadata confirmed the hard link and original file share the same underlying data location.

### cat hardlink.txt
```text
Sample content for link analysis
```
The hard link still provided the file contents after the original name was removed, showing the data remained accessible.

### cat symlink.txt
```text
cat: symlink.txt: No such file or directory
```
The symlink failed after the original file was deleted, demonstrating that symbolic links depend on the target path.
