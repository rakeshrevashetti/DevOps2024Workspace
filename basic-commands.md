# Basic Linux Commands

## 1. Navigation Commands
- `pwd`: Print working directory (shows the current directory path).
- `cd <directory>`: Change the current directory.
  - Example: `cd /home/user/Documents`
- `ls`: List files and directories in the current directory.
  - `ls -l`: List with details (permissions, size, etc.).
  - `ls -a`: Show hidden files (files starting with a dot).

## 2. File and Directory Management
- `mkdir <directory_name>`: Create a new directory.
  - Example: `mkdir myfolder`
- `rmdir <directory_name>`: Remove an empty directory.
  - Example: `rmdir myfolder`
- `rm <file_name>`: Remove a file.
  - Example: `rm file.txt`
- `rm -r <directory_name>`: Remove a directory and its contents.
  - Example: `rm -r myfolder`
- `cp <source> <destination>`: Copy files or directories.
  - Example: `cp file1.txt file2.txt`
- `mv <source> <destination>`: Move or rename files and directories.
  - Example: `mv oldname.txt newname.txt`

## 3. Viewing Files and File Contents
- `cat <file_name>`: View the content of a file.
  - Example: `cat file.txt`
- `less <file_name>`: View large files page by page.
  - Example: `less file.txt`
- `head <file_name>`: Display the first 10 lines of a file.
  - Example: `head file.txt`
- `tail <file_name>`: Display the last 10 lines of a file.
  - Example: `tail file.txt`

## 4. File Permissions and Ownership
- `chmod <permissions> <file_name>`: Change file permissions.
  - Example: `chmod 755 script.sh` (gives read/write/execute to the owner, and read/execute to others).
- `chown <user>:<group> <file_name>`: Change file owner and group.
  - Example: `chown user:group file.txt`

## 5. System Information
- `df`: Show disk space usage.
- `du`: Show directory space usage.
  - Example: `du -sh *` (show size of each file/folder in the current directory).
- `top`: Display system resource usage (CPU, memory).
- `free`: Show memory usage.
- `uname -a`: Show system information (kernel version, OS type).

## 6. Process Management
- `ps`: Show currently running processes.
- `kill <pid>`: Terminate a process by its PID (Process ID).
  - Example: `kill 1234`
- `killall <process_name>`: Terminate all processes with a specific name.
  - Example: `killall firefox`
