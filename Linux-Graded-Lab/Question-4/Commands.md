# Question 4 - File Access and I/O

## Command

```bash
echo "This is standard output" > output.txt
```
### Purpose
I used this to send text into a file instead of showing it on the screen.
### Observation
The text was written into output.txt and the file was created if it did not exist. I could check the file afterward.

## Command

```bash
echo "This is appended output" >> output.txt
```
### Purpose
I appended more text to the same file.
### Observation
The new line was added to the end of output.txt. The previous content stayed intact.

## Command

```bash
cat < output.txt
```
### Purpose
I used input redirection to display the file contents.
### Observation
The file contents appeared on the screen. It showed the text I had written to output.txt.

## Command

```bash
ls /nonexistent 2> error.log
```
### Purpose
I sent the error message from a failed ls command into a file.
### Observation
No error was shown on the terminal. The message was captured in error.log.

## Command

```bash
echo "Data sent through tee" | tee combined.txt
```
### Purpose
I wanted to write output to both the screen and a file.
### Observation
The text appeared on the terminal and was saved to combined.txt at the same time.

## Command

```bash
ulimit -n
```
### Purpose
I checked how many files the shell can keep open at once.
### Observation
The command printed a number. I noted it for the report.

## Command

```bash
exec 3>fd_demo.txt
echo "Using file descriptor 3" >&3
exec 3>&-
```
### Purpose
I tested writing to a custom file descriptor.
### Observation
The text was written into fd_demo.txt through descriptor 3. Then I closed the descriptor.

## Command

```bash
lsof +D .
```
### Purpose
I checked which files were open in the current directory.
### Observation
The list showed a few open files and processes. It helped me see file activity in the folder.
