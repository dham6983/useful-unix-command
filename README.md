# useful-unix-command 
Always run this commands and see the output by yourself to get used to with the output. I will keep adding more sections here.This is for my personal use.


## ls commands ##

`ls`- list all files in a directory

`ls -l` - long list all files.

`ls -lr` - list all files in reverse order

`ls -lt` - list all files and sort by modified date

`ls -lrt` - list all files and sort by modified date with recently modified files at the last.

`ls <filename regex>` - List file with regex. Refer the example below

#### Example

```
ls sourav*

```

## ps commands ##

`ps -ef` list all running processes.

`ps -ef | grep "process name"` list all process name matching the grep input.

## viewing files ##

`more <filename>` view a file in the terminal window.

`less <filename>` anotherway to view a file in the terminal window.

`cat <filename>` view entire file in the terminal window.


## cp commands ##

`cp <source filename> <destination file name>` Copy source to destination.

`cp -R <source directory name> <destination>` copying file recursively.

## scp commands ##

`scp <source filename> <destination file name>` copying files between servers

`scp <filename> username@<remote-ip-address>:<destination-path>`  Copying file into remote server from local

`scp username@<remote-ip-address>:<source-file-path-name> <destination-path>`  Copying file from remote to local

`scp username@<source-remote-ip-address>:<source-file-path-name> username@<destination-remote-ip-address>:<source-file-path-name>` Copying file between two remote servers.

## Miscellaneous command ##

`cd <path to dir>` change to directory.

`clear` clears the screen

`vi <filename>` create or edit a new file using vi editor. 
### Note : vi itself is a different beast. I will share vi shortcuts later.

`netstat -an` shows the network output for current environment.

`history` list the entire history of all your typed commands for this session.

`chown <owner>:<group> <filename` change ownership of a file.

`id` identify the current user.

`su <username>` switch to the specified user name.

`sudo <programe name or cmd` switch to root and execute the command.

`pwd` - find the current working directory

## grep commands ##

`grep -ir <regex> <filname>` 

- `grep` : Serach a regex pattern in a file
- `-i`   : case insensitive
- `-r`.  : recursively 

## lspci commands ##

`lspci` : List all harwardware components in the system

`lspci -v | less` : Details list of all hardware components in the the system.

## Disk usage ##

`du -hc /home/daygeek/Documents/ | sort -rh | head -20`

- `du`: It’s a command
- `-h`: Print sizes in human readable format (e.g., 1K, 234M, 2G)
- `-c`: Produce a grand total
- `/home/daygeek/Documents/`: The path of directory
- `sort -rh`: Sort the results with numerical value
- `head -20`: Output the first 20 lines result

`du -h --max-depth=0 /home/daygeek/Documents/` : first level only

`ncdu /home/daygeek/Documents/` : Using ncurses method

`tree --du -h /opt/ktube-media-downloader` : Using tree method
