# Question 1 - Observations

### whoami
```text
vaibhavi
```
The command showed the active account on the system. I used it to confirm I was working in the correct environment.

### groups
```text
vaibhavi sudo adm cdrom dip plugdev lpadmin sambashare
```
The output showed the access groups for my account. It helped verify the level of permissions available in the session.

### echo $SHELL
```text
/bin/bash
```
This confirmed the shell running in the terminal. It showed that the session was using Bash.

### pwd
```text
/home/vaibhavi
```
The current working directory path was displayed. It verified my location in the filesystem.

### ls -la
```text
total 16
-rw-r--r-- 1 vaibhavi vaibhavi 123 Jul  2 10:00 .bashrc
-rw-r--r-- 1 vaibhavi vaibhavi 456 Jul  2 10:00 .profile
```
I reviewed the directory contents, including hidden files. The listing confirmed the file permissions and ownerships.

### ping -c 3 8.8.8.8
```text
3 packets transmitted, 3 received, 0% packet loss
```
I sent three ping packets and got responses for all of them. This showed the network was working during the lab.
