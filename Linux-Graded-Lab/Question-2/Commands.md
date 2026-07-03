# Question 2 - Secure Workspace

## Command

```bash
mkdir -p ~/Linux-Lab-Workspace/{docs,notes,archive}
```
### Purpose
I used this to create a workspace with separate folders.
### Observation
The command made the docs, notes, and archive folders in one step. I could see the new structure right away.

## Command

```bash
touch ~/Linux-Lab-Workspace/docs/plan.txt ~/Linux-Lab-Workspace/notes/todo.txt
```
### Purpose
I created the files that I would use for notes and planning.
### Observation
Both files were created without any output. I checked the folder and the files were there.

## Command

```bash
ls -l ~/Linux-Lab-Workspace
```
### Purpose
I wanted to check the permissions and contents of the workspace folder.
### Observation
The list showed the folders and files with their permission bits. It confirmed everything was created correctly.

## Command

```bash
chmod u+rwx,g+rx,o-rwx ~/Linux-Lab-Workspace/docs/plan.txt
```
### Purpose
I changed the plan file permissions so I could edit it and keep others out.
### Observation
The file was updated to allow owner access and remove access for others. The change was visible in the file listing.

## Command

```bash
chmod 640 ~/Linux-Lab-Workspace/notes/todo.txt
```
### Purpose
I set the todo file to be readable by group but writable only by me.
### Observation
The permission mode was applied successfully. The rights looked correct in the output.

## Command

```bash
stat -c '%n %U %G %a' ~/Linux-Lab-Workspace/docs/plan.txt ~/Linux-Lab-Workspace/notes/todo.txt
```
### Purpose
I checked the owner and permission bits for both files.
### Observation
The output showed the file owner, group, and numeric permissions. It matched the values I expected.

## Command

```bash
umask
```
### Purpose
I checked the current default file permission mask.
### Observation
The command printed a number that controls default permissions. I noted it for the report.

## Command

```bash
chmod --help | head
```
### Purpose
I opened the first part of chmod help to see how permission changes work.
### Observation
The help text showed usage and examples. It was useful for confirming the correct chmod syntax.
