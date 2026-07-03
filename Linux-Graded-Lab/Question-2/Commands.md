# Question 2 - Secure Workspace

## Command

```bash
mkdir -p ~/Linux-Lab-Workspace/{docs,notes,archive}
```
### Purpose
I created a dedicated workspace structure for organizing lab documents.
### Result
The command built the docs, notes, and archive directories in one step so I could continue with the task.

## Command

```bash
touch ~/Linux-Lab-Workspace/docs/plan.txt ~/Linux-Lab-Workspace/notes/todo.txt
```
### Purpose
I prepared the report and task-tracking files needed for the workspace.
### Result
Both files were created successfully and were available in the workspace.

## Command

```bash
ls -l ~/Linux-Lab-Workspace
```
### Purpose
I checked the workspace contents and the file permission settings.
### Result
The directory listing confirmed the folders existed and showed their permissions clearly.

## Command

```bash
chmod u+rwx,g+rx,o-rwx ~/Linux-Lab-Workspace/docs/plan.txt
```
### Purpose
I restricted access to the plan file so only I could modify it.
### Result
The permission change applied to plan.txt, allowing owner read/write/execute while restricting others.

## Command

```bash
chmod 640 ~/Linux-Lab-Workspace/notes/todo.txt
```
### Purpose
I adjusted the todo file permissions to improve security.
### Result
The file was set to owner read/write and group read only, with no access for others.

## Command

```bash
stat -c '%n %U %G %a' ~/Linux-Lab-Workspace/docs/plan.txt ~/Linux-Lab-Workspace/notes/todo.txt
```
### Purpose
I verified ownership and permission bits for the workspace files.
### Result
The output showed both files were owned by my account with the expected permission modes.

## Command

```bash
umask
```
### Purpose
I checked the default mask that controls permissions for newly created files.
### Result
It displayed the current umask value used for the session.

## Command

```bash
chmod --help | head
```
### Purpose
I reviewed the chmod manual page for the command syntax.
### Result
The first part of the help output confirmed the permission change options and usage.
