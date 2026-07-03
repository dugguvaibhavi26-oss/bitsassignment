# Question 3 - File System and Link Analysis

## Command

```bash
echo "Sample content for link analysis" > sample.txt
```
### Purpose
I created a simple file to use for the link tests.
### Observation
The file was written without any output. I could check it later with cat or ls.

## Command

```bash
ln sample.txt hardlink.txt
```
### Purpose
I made a hard link to the original file.
### Observation
The hard link was created with the same content. It should act like another name for the same file.

## Command

```bash
ln -s sample.txt symlink.txt
```
### Purpose
I created a symbolic link that points to the sample file.
### Observation
The symlink appeared in the folder and pointed back to sample.txt. It shows the target path rather than duplicating the file.

## Command

```bash
ls -li sample.txt hardlink.txt symlink.txt
```
### Purpose
I wanted to compare inode numbers for the files.
### Observation
The hard link shared the same inode with the original file. The symlink had a different inode number.

## Command

```bash
stat sample.txt hardlink.txt symlink.txt
```
### Purpose
I checked the file metadata for the links and original file.
### Observation
The output showed size, inode, and timestamps. It confirmed the file relationships for the report.

## Command

```bash
rm sample.txt
```
### Purpose
I removed the original file to test link behavior.
### Observation
The original name disappeared from the directory. I then checked whether the links still worked.

## Command

```bash
cat hardlink.txt
```
### Purpose
I read the hard link after deleting the original file.
### Observation
The hard link still showed the original text. That proved it still pointed to the same data.

## Command

```bash
cat symlink.txt
```
### Purpose
I tried to read the symbolic link after deleting its target.
### Observation
The symlink failed because the target was gone. That showed the symlink points to a file path rather than content.
