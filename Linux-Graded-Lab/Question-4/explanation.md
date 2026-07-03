# Question 4 - Observations

### echo "This is standard output" > output.txt
```text
No output if the command succeeds.
```
The command redirected console output into a file, creating output.txt with the given text.

### cat < output.txt
```text
This is standard output
This is appended output
```
Input redirection displayed the contents of output.txt, showing both lines saved earlier.

### ls /nonexistent 2> error.log
```text
No output on the terminal if redirection works.
```
The error from the failing ls command was captured in error.log instead of being displayed.

### echo "Data sent through tee" | tee combined.txt
```text
Data sent through tee
```
The line was output to the screen and written into combined.txt at the same time.

### ulimit -n
```text
1024
```
The shell reported the limit on open file descriptors for the current process.

### lsof +D .
```text
COMMAND PID USER FD TYPE DEVICE SIZE/OFF NODE NAME
```
This command listed open file handles in the current directory, useful for tracking active file usage.
