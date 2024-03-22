# Linux

## Some relevant commands

<pre>
-connecting to a linux terminal via windows> ssh -l [username] [ip address]

-command promts and geting back: ctrl + c

- whoami - shows your username
- hostname - name of the machine
- top - monitorng procesess in real time
</pre>

## 44. Files system Structture and its Description

<pre>
boot,
root - root user home directory
dev - system devices
etc - Config files
/bin -> /usr/bin - everyday user commands
/sbin -> /usr/sbin - System/filesystem commands
/opt -Optional add-on apllication (Not partn of OS apps)
/proc - Running process (only exist inj Memory)
/lib -> usr/lib - C programming library files needed by commands and apps
/tmp - Direcriy for temporary files
/home - Directory for user
/var - System logs
/run - temporary runtime files like PID
/mnt - To mount external filesystem (e.g. NFS)
/media - For cdrom mounts
</pre>

## 45. File System Navigation Commands

<pre>
cd - change directory
pwd - print working directory
ls -l (ls -ltr) - listing the content of the directory with their properties
-rw-r.... - minus symbol in the begining means a file
drwxr - d means directory
</pre>

## 46. Linux File or Directory Properties

<pre>
lrwxrwxrwx - link
</pre>

## 47. Linux File Types

<pre>
|File Symbol     |     Meannig | 
|---------------|:-------------:|
| -             | Regular file|
| d             | Directory   |
| l             | link        |
| c             | Special file or device|
| s             | socket       |
| p             | Name pipe |
| b             | Block device|
</pre>
