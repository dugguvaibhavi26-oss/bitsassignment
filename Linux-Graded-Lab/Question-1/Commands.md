# Question 1 - Linux Environment Verification

## Command

```bash
whoami
```
### Purpose
I used this command to confirm which user profile the shell was running under.
### Result
The output displayed my current username and verified the session was active for the correct account.

## Command

```bash
groups
```
### Purpose
I checked the group memberships assigned to my Linux account.
### Result
The command returned a list of groups that define my system privileges and access.

## Command

```bash
echo $SHELL
```
### Purpose
I verified the active shell environment for this session.
### Result
The output showed /bin/bash, confirming that Bash was the login shell.

## Command

```bash
pwd
```
### Purpose
I confirmed the present working directory for the lab tasks.
### Result
The command printed the full path currently in use, ensuring I was in the correct directory.

## Command

```bash
ls -la
```
### Purpose
I listed all entries, including hidden files, in the current folder.
### Result
The listing showed file names, ownership, permissions, and hidden files so I could inspect the environment.

## Command

```bash
ping -c 3 8.8.8.8
```
### Purpose
I verified the network connection by sending ping packets to a public DNS server.
### Result
All three packets were returned successfully, showing that the network was reachable.
