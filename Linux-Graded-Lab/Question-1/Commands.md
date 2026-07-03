# Question 1 - Linux Environment Verification

## Command

```bash
whoami
```
### Purpose
I ran this to check which user account was active in the terminal.
### Observation
It showed the username that I was logged in as. I used this to confirm I was working in the right environment.

## Command

```bash
groups
```
### Purpose
I wanted to see which groups my account belonged to.
### Observation
The output listed several groups on one line. It helped me understand my access rights in the system.

## Command

```bash
echo $SHELL
```
### Purpose
I used this to find the current shell I was using.
### Observation
The result showed the shell path, like /bin/bash. This told me the session was running the expected shell.

## Command

```bash
pwd
```
### Purpose
I ran this to check my current working directory.
### Observation
It printed the full path where I was working. This confirmed I was in the right folder for the lab.

## Command

```bash
ls -la
```
### Purpose
I listed all files and folders to see what was in the current directory.
### Observation
The output included hidden files and showed permissions and sizes. I could see the layout of the folder clearly.

## Command

```bash
ping -c 3 8.8.8.8
```
### Purpose
I tested the network connection to a public IP address.
### Observation
All packets were replied to with no loss. This showed the network connection was working.
