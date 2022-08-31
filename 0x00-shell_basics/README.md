 # Bash Shell Scripting Project

**directory structure**
```
.alx-system_engineering-devops
├── 0x00-shell_basics
|   ├── 0-current_working_directory
|   ├── 1-listit
|   ├── 2-bring_me_home
|   ├── 3-listfiles
|   ├── 4-listmorefiles
|   ├── 5-listfilesdigitonly
|   ├── 6-firstdirectory
|   ├── 7-movethatfile
|   ├── 8-firstdelete
|   ├── 9-firstdirdeletion
|   ├── 10-back
|   ├── 11-lists
|   ├── 12-file_type
|   ├── 13-symbolic_link
|   ├── 14-copy_html
│   └── README.md
└── README.md
```



## Task 0
Create a file called **0-current_working_directory**
Write  a script that prints the absolute path name of the current working directory.

**Example:**
```
$ ./0-current_working_directory
/root/alx-system_engineering-devops/0x00-shell_basics
$
```
## Task 1
Create a file called **1-listit**
Displaying the contents list of your current directory.
** Example: **
```
$ ./1-listit
Applications    Documents   Dropbox Movies Pictures
Desktop Downloads   Library Music Public
$
```
## Task2
create a file called **2-bring_me_home**
Write a script that changes the working directory to the user’s home directory.
-   You are not allowed to use any shell variables

**Example:**
```
julien@ubuntu:/tmp$ pwd
/tmp
julien@ubuntu:/tmp$ echo $HOME
/home/julien
julien@ubuntu:/tmp$ source ./2-bring_me_home
julien@ubuntu:~$ pwd
/home/julien
julien@ubuntu:~$ 
```
## Task 3
Create a file called **3-listfiles**
Display current directory contents in a long format
**Example:**
```
$ ./3-listfiles
total 32
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:19 0-current_working_directory
-rwxr-xr-x@ 1 sylvain staff 19 Jan 25 00:23 1-listit
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:29 2-bring_me_home
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:39 3-listfiles
$
```
## task 4
create file called **4-listmorefiles**
Display current directory contents, including hidden files (starting with  `.`). Use the long format.

**Example:**

```
$ ./4-listmorefiles
total 32
drwxr-xr-x@ 6 sylvain staff 204 Jan 25 00:29 .
drwxr-xr-x@ 43 sylvain staff 1462 Jan 25 00:19 ..
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:19 0-current_working_directory
-rwxr-xr-x@ 1 sylvain staff 19 Jan 25 00:23 1-listit
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:29 2-bring_me_home
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:39 3-listfiles
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:41 4-listmorefiles
$
```
## Task 5
Create a file called **5-listfilesdigitonly**
Display current directory contents.

-   Long format
-   with user and group IDs displayed numerically
-   And hidden files (starting with .)

**Example:**
```
$ ./5-listfilesdigitonly
total 32
drwxr-xr-x@ 6 501 20 204 Jan 25 00:29 .
drwxr-xr-x@ 43 501 20 1462 Jan 25 00:19 ..
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:19 0-current_working_directory
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:23 1-listfiles
-rwxr-xr-x@ 1 501 20 19 Jan 25 00:29 2-bring_me_home
-rwxr-xr-x@ 1 501 20 20 Jan 25 00:39 3-listfiles
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:41 4-listmorefiles
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:43 5-listfilesdigitonly
$
```

## Task 6
Create a file called **6-firstdirectory**
Create a script that creates a directory named  `my_first_directory`  in the  `/tmp/`  directory.

**Example:**

```
$ ./6-firstdirectory
$ file /tmp/my_first_directory/
/tmp/my_first_directory/: directory
$
```
## Task 7
Create a file called **7-movethatfile**
Move the file  `betty`  from  `/tmp/`  to  `/tmp/my_first_directory`.

**Example:**

```
$ ./7-movethatfile
$ ls /tmp/my_first_directory/
betty
$
```
## Task 8
Create a file called **8-firstdelete**
Delete the file  `betty`.

-   The file  `betty`  is in  `/tmp/my_first_directory`

Example:

```
$ ./8-firstdelete
$ ls /tmp/my_first_directory/
$
```
## task 9
Create a file called **9-firstdirdeletion**
Delete the directory  `my_first_directory`  that is in the  `/tmp`  directory.
**Example:**
```
$ ./9-firstdirdeletion
$ file /tmp/my_first_directory
/tmp/my_first_directory: cannot open `/tmp/my_first_directory' (No such file or directory)
$
```
## Task 10
create a file called **10-back**
Write a script that changes the working directory to the previous one.

```
julien@ubuntu:/tmp$ pwd
/tmp
julien@ubuntu:/tmp$ cd /var
julien@ubuntu:/var$ pwd
/var
julien@ubuntu:/var$ source ./10-back
/tmp
julien@ubuntu:/tmp$ pwd
/tmp
```
## Task 11
Create a file called **11-lists**
Write a script that lists all files (even ones with names beginning with a period character, which are normally hidden) in the current directory and the parent of the working directory and the  `/boot`  directory (in this order), in long format.

## Task 12
Create a file called **12-file_type**
Write a script that prints the type of the file named  `iamafile`. The file  `iamafile`  will be in the  `/tmp`  directory when we will run your script.

Example

```
ubuntu@ip-172-31-63-244:~$ ./12-file_type
/tmp/iamafile: ELF 64-bit LSB  executable, x86-64, version 1 (SYSV), dynamically linked (uses shared libs), for GNU/Linux 2.6.24, BuildID[sha1]=bd39c07194a778ccc066fc963ca152bdfaa3f971, stripped
```

## Task 13
Create a file called **13-symbolic_link**
Create a symbolic link to  `/bin/ls`, named  `__ls__`. The symbolic link should be created in the current working directory.

```
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la
total 144
drwxrwxr-x  2 ubuntu ubuntu   4096 Sep 20 03:24 .
drwxrwxrwt 12 root   root   139264 Sep 20 03:24 ..
ubuntu@ip-172-31-63-244:/tmp/sym$./13-symbolic_link
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la
total 144
drwxrwxr-x  2 ubuntu ubuntu   4096 Sep 20 03:24 .
drwxrwxrwt 12 root   root   139264 Sep 20 03:24 ..
lrwxrwxrwx  1 ubuntu ubuntu      7 Sep 20 03:24 __ls__ -> /bin/ls
```
## Task 14
Create a file called **14-copy_html**
Create a script that copies all the HTML files from the current working directory to the parent of the working directory, but only copy files that did not exist in the parent of the working directory or were newer than the versions in the parent of the working directory.

You can consider that all HTML files have the extension  `.html 
