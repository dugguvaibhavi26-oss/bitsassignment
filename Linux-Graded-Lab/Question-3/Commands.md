# Question 3 - File System and Link Analysis

## Command

```bash
echo "Sample content for link analysis" > sample.txt
```
### Purpose
I created a sample data file that would be used to compare link behavior.
### Result
The file was created with the expected text and could be inspected with standard tools.

## Command

```bash
ln sample.txt hardlink.txt
```
### Purpose
I created a hard link to the sample file so I could compare inode sharing.
### Result
hardlink.txt was created successfully and pointed to the same underlying data as sample.txt.

## Command

```bash
ln -s sample.txt symlink.txt
```
### Purpose
I created a symbolic link to the sample file to observe its referencing behavior.
### Result
symlink.txt was added and pointed to sample.txt rather than containing its own data.

## Command

```bash
ls -li sample.txt hardlink.txt symlink.txt
```
### Purpose
I compared the inode and file information for the files and links.
### Result
The hard link shared the same inode as sample.txt, while the symlink had a distinct inode and target path.

## Command

```bash
stat sample.txt hardlink.txt symlink.txt
```
### Purpose
I checked the metadata for the sample file and both links.
### Result
The output confirmed the shared data for sample.txt and hardlink.txt, while symlink.txt showed link metadata.

## Command

```bash
rm sample.txt
```
### Purpose
I deleted the original file to test how each link behaved after removal.
### Result
The sample file name was removed, leaving the links behind.

## Command

```bash
cat hardlink.txt
```
### Purpose
I verified that the hard link still provided access to the file contents.
### Result
hardlink.txt continued to display the original text, proving the data remained available.

## Command

```bash
cat symlink.txt
```
### Purpose
I checked whether the symbolic link still resolved after its target was deleted.
### Result
symlink.txt failed because the target was no longer present, demonstrating broken symlink behavior.
