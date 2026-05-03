# Bash Basics

A quick reference guide for essential Bash commands, hotkeys, and tips.

## Basic Commands

| Command            | Description                | Example                                          |
| ------------------ | -------------------------- | ------------------------------------------------ |
| `pwd`              | Print Working Directory    | `pwd`                                            |
| `ls`               | List directory contents    | `ls -la` (show hidden files)                     |
| `cd`               | Change Directory           | `cd /path` `cd ~` `cd -` `cd ..`                 |
| `echo`             | Print text or variables    | `echo "Hello World"`<br>`echo $PATH`             |
| `man`              | Manual pages for commands  | `man ls`                                         |
| `help`             | Help for Bash builtins     | `help cd`                                        |
| `clear` / `Ctrl+L` | Clear terminal screen      | `clear`                                          |
| `history`          | Show command history       | `history` (show all)<br>`!123` (run command 123) |
| `date`             | Display current date/time  | `date`                                           |
| `whoami`           | Current username           | `whoami`                                         |
| `uname`            | System information         | `uname -a`                                       |
| `ps`               | Process status             | `ps aux`                                         |
| `top` / `htop`     | Interactive process viewer | `top`                                            |
| `kill`             | Terminate process          | `kill 1234` (graceful)<br>`kill -9 1234` (force) |

## Redirection & Pipes

| Operator | Description                           | Example                                                            |
| -------- | ------------------------------------- | ------------------------------------------------------------------ |
| `\|`     | Pipe: send output to another command  | `ls -la \| grep "txt"` (filter results)<br>`ps aux \| grep python` |
| `>`      | Redirect output to file (overwrite)   | `echo "Hello" > file.txt`                                          |
| `>>`     | Redirect output to file (append)      | `echo "World" >> file.txt`                                         |
| `<`      | Redirect file as input                | `wc -l < file.txt`                                                 |
| `2>`     | Redirect error output                 | `command 2> errors.log`                                            |
| `&>`     | Redirect all output (stdout + stderr) | `command &> output.log`                                            |

### Common Pipe Examples

```bash
# Filter output
ls -la | grep "\.txt$"

# Count results
ls -la | wc -l

# Sort output
ps aux | sort -k 3 -r  # sort by CPU usage

# Chain multiple commands
dmesg | grep -i error | tail -20
```

## File & Directory Management

| Command         | Description                           | Example                                                                  |
| --------------- | ------------------------------------- | ------------------------------------------------------------------------ |
| `touch`         | Create empty file or update timestamp | `touch file.txt`                                                         |
| `mkdir`         | Make directory                        | `mkdir dir` (single)<br>`mkdir -p dir/subdir` (parents)                  |
| `cp`            | Copy files/directories                | `cp file.txt /backup/` (file)<br>`cp -r dir/ /backup/` (recursive)       |
| `mv`            | Move or rename files/directories      | `mv old.txt new.txt` (rename)<br>`mv file.txt /target/` (move)           |
| `rm`            | Remove files/directories              | `rm file.txt` (file)<br>`rm -rf dir/` (recursive, force)                 |
| `rmdir`         | Remove empty directory                | `rmdir dir`                                                              |
| `cat`           | Concatenate and display file content  | `cat file.txt`                                                           |
| `less` / `more` | View file content page by page        | `less file.txt`                                                          |
| `head`          | Display first lines                   | `head -n 10 file.txt`                                                    |
| `tail`          | Display last lines                    | `tail -f file.log` (follow)                                              |
| `grep`          | Search text in files                  | `grep "pattern" file.txt` (file)<br>`grep -r "pattern" dir/` (recursive) |
| `find`          | Search files/directories              | `find . -name "*.txt"`                                                   |
| `wc`            | Word/Line/Character count             | `wc -l file.txt`                                                         |
| `diff`          | Compare files                         | `diff file1.txt file2.txt`                                               |
| `chmod`         | Change file permissions               | `chmod 755 script.sh`                                                    |
| `chown`         | Change file owner                     | `chown user:group file.txt`                                              |
| `ln`            | Create links                          | `ln -s target linkname` (symbolic)                                       |

## Detailed Command Examples

### Navigation & Information

```bash
# Current location and listing
pwd
ls -la --color=auto
ls -lh  # human readable sizes

# Directory navigation
cd /etc
cd ~ # go home
cd ../..  # go up two levels
```
