# Question 4 - File Access and I/O

## Command

```bash
echo "This is standard output" > output.txt
```
### Purpose
I redirected normal output to a file to demonstrate output capture.
### Result
The string was saved into output.txt, creating the file if needed.

## Command

```bash
echo "This is appended output" >> output.txt
```
### Purpose
I added more text to the existing output file without overwriting it.
### Result
The new line was appended to output.txt, preserving the original content.

## Command

```bash
cat < output.txt
```
### Purpose
I used input redirection to read the file contents through cat.
### Result
The contents of output.txt were printed to the terminal successfully.

## Command

```bash
ls /nonexistent 2> error.log
```
### Purpose
I redirected the standard error from a failing command into a log file.
### Result
No error text appeared on-screen; the failure message was written to error.log.

## Command

```bash
echo "Data sent through tee" | tee combined.txt
```
### Purpose
I demonstrated writing output to both the terminal and a file at the same time.
### Result
The message appeared on-screen and was saved into combined.txt.

## Command

```bash
ulimit -n
```
### Purpose
I inspected the shell's open-file descriptor limit.
### Result
The command printed the current maximum number of open files.

## Command

```bash
exec 3>fd_demo.txt
echo "Using file descriptor 3" >&3
exec 3>&-
```
### Purpose
I experimented with opening a custom file descriptor and writing through it.
### Result
The text was written to fd_demo.txt via descriptor 3, then the descriptor was closed.

## Command

```bash
lsof +D .
```
### Purpose
I viewed the list of processes with files open in the current directory.
### Result
The command output showed active file handles in the folder.
