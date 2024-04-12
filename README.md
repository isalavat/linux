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

| File Symbol |        Meannig         |
| ----------- | :--------------------: |
| -           |      Regular file      |
| d           |       Directory        |
| l           |          link          |
| c           | Special file or device |
| s           |         socket         |
| p           |       Name pipe        |
| b           |      Block device      |

## 48. What is root?

<pre>
There 3 types of root:

1. Root account
2. Root directory - /
3. Root home directory - the root user accout directory located in /root
</pre>

## 49. Changing Password

<pre>
Command = passwd userid (old, new, confirm new)
</pre>

## 50. Absolute and Relative Paths

<pre>
Absolute path cd /var/log
Relative path cd log
/ - root directory

su - : root user
</pre>

## 51. Creating Files and Directories (touch, cp, vi, mkdir)

<pre>
  Creating files
    touch
    cp (copy command)
    vi (creates a file and opens it in a editor)
      :wq!
  
  Creating Diretories
    mkdir
</pre>

## 52. Copying directories

<pre>
  cp -R source destination
  mv file.txt /home/username/documents - moving file to detination folder
</pre>

## 53. Finding files and directories (find, locate)

<pre>
  find . -name "kramer"  - . is a relative path pointing to current directory
  find / -name "ifcfg-enp0s3"
  Help - man find 

  
</pre>

## 54. Difference Between Find and Locate Commands

<pre>
  locate example.txt
  
  The locate command in Unix-like operating systems is a quick and efficient way to 
  search for files by their name. Unlike the find command, which searches the file 
  system in real-time, locate searches a database of indexed file paths, making it 
  much faster for finding files when you know their names or partial names. However, 
  because locate relies on a database that is periodically updated (usually once a 
  day via a cron job), it may not always reflect the most current state of the file 
  system.

  sudo updatedb  - updating db

</pre>

## 55. WildCards (\*, ?, ^, [])

<pre>
  touch abcd{1..9}-xyz > creates 9 files with a given wildcard
  rm a* > removing all files starting with "a"
  ls -l ?bcd* > listing files with a given wildcard 
</pre>

## 56. Soft and Hard Links (ln)

<pre>
  inode - Pointer or number of a file on the hard disk
  Soft Link - Link will be removed if file is removed or renamed
  Hard Link - Deleting renaming or moving the original file will not affect the hard link
    ln or ln -s (for a soft link)
    lrwxr... > l stands for a link
  
  echo "Hulk is super" > hulk: This command uses echo to print the string "Hulk is super" and then redirects the output (>) into a file named hulk. If the file hulk already exists, it will be overwritten without warning. If the file doesn't exist, it will be created.

  cat hulk: This command uses cat to display the contents of the file named hulk on 
  the terminal. If the previous command was executed successfully, this command will 
  output "Hulk is super" to the screen.

  ls -li > listing files including the information about inode
</pre>

## 60. Linux Command Syntax

<pre>
  rm -f filename > deleting a file
  rm -r foldername > deleting a folder
  man ls > listing command manual
  
</pre>

## 61. Files and Directory (chmod)

<pre>
  3 types of permissions
   r - read
   w - write
   x - execute
  each permission (rwx) can be controlled at three levels:
    u - user = yourself
    g - group = can be people in the same project
    o - other = everyone on the system 
  ls -l = it lists permissions
    - rwxrwxrwx
  ls = lists files and dirs only
  
  Adding Permissions

  Add execute permission for the owner:
   chmod u+x filename
  Add read and write permissions for the group:
    chmod g+rw filename
  Remove execute permission from others:
    chmod o-x filename
  
  Setting Permissions
  Set the permissions so that the owner can read and write, the group can read, and 
  others have no permissions:
    chmod u=rw,g=r,o= filename  
</pre>
