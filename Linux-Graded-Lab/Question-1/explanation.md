# Question 1 - Observations

### whoami
```text
student
```
I checked the active user and confirmed the session was under the expected account.

### groups
```text
student sudo adm cdrom dip plugdev lpadmin sambashare
```
The group list showed the current user's access groups. It matched what I expected for a standard Linux account.

### echo $SHELL
```text
/bin/bash
```
This showed the shell I was using. I confirmed that the terminal was running Bash.

### pwd
```text
/home/student
```
The current directory path was displayed. I used it to confirm my location in the filesystem.

### ls -la
```text
total 16
-rw-r--r-- 1 student student 123 Jul  2 10:00 .bashrc
-rw-r--r-- 1 student student 456 Jul  2 10:00 .profile
```
I saw all files in the folder, including hidden ones. The listing also showed permissions and file details.

### ping -c 3 8.8.8.8
```text
3 packets transmitted, 3 received, 0% packet loss
```
I sent three ping packets and got responses for all of them. This showed the network was working during the lab.
