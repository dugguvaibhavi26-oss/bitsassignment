# Question 4 - Observations

### echo "This is standard output" > output.txt
```text
No output if the command succeeds.
```
The file was created and it did not print anything to the terminal. I used ls to check that output.txt existed.

### cat < output.txt
```text
This is standard output
This is appended output
```
The redirected input showed the contents of output.txt. It confirmed both lines were saved in the file.

### ls /nonexistent 2> error.log
```text
No terminal output if the error is redirected successfully.
```
The error message was hidden from the terminal. I then opened error.log to see the failure text.

### echo "Data sent through tee" | tee combined.txt
```text
Data sent through tee
```
The text appeared on the screen and got saved to combined.txt. I verified the file had the same line.

### ulimit -n
```text
1024
```
The shell showed the open-file limit. I wrote down the number for the lab report.

### lsof +D .
```text
COMMAND PID USER FD TYPE DEVICE SIZE/OFF NODE NAME
```
The command listed open files in the current directory. It helped me see what processes were using files there.
