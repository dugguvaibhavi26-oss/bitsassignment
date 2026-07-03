# Question 2 - Observations

### mkdir -p ~/Linux-Lab-Workspace/{docs,notes,archive}
```text
No output if the directories are created successfully.
```
The folders were created without errors. I checked the workspace and saw all three directories.

### ls -l ~/Linux-Lab-Workspace
```text
drwxr-xr-x 2 student student 4096 Jul  2 10:30 docs
drwxr-xr-x 2 student student 4096 Jul  2 10:30 notes
drwxr-xr-x 2 student student 4096 Jul  2 10:30 archive
```
The list showed the new directories and their access modes. It confirmed the workspace structure was set up right.

### chmod 640 ~/Linux-Lab-Workspace/notes/todo.txt
```text
No output if the command succeeds.
```
The file permissions changed quietly. I later verified the mode was correct.

### umask
```text
0022
```
The default permission mask was shown. I used it to understand the default access for new files.

### Permission Model Summary
Owner means the user who created the file. Group is for other users in the same group. Others is anyone else on the system. The letters r, w, and x mean read, write, and execute.
