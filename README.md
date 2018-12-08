# basic linux commands 
## [What is the terminal?](https://itconnect.uw.edu/learn/workshops/online-tutorials/web-publishing/what-is-a-terminal/)
> **Terminals**, also known as command lines or consoles, allow us to accomplish and automate tasks on a computer without the > use of a graphical user interface. Using a terminal allows us to send simple text commands to our computer to do things like > navigate through a directory or copy a file, and form the basis for many more complex automations and programming skills. 

## 1. open a new terminal 
(1). *Open* the Dash by clicking the Ubuntu icon in the upper-left, type `terminal`, and select the Terminal application from the results that appear.

(2). Hit the keyboard *shortcut*: **Ctrl** + **Alt** + **T**

## 2. man command
**man** - an interface to the on-line reference manuals.
```
binli@ubuntu:~$ man man

DESCRIPTION
   man is the system's manual pager.  Each page argument given to man is normally the name of a program, utility or function.  The manual page  associated with each of these arguments is then found and displayed.  A section, if provided, will direct man to look only in that section of the manual.  
```
## 3. pwd command
This command prints the location of your current working directory. It's important to know actually where you're before going to a parent or sub directories.
```
binli@ubuntu:~$ pwd
/home/binli
binli@ubuntu:~$ 
```
"~" - represent the home folder of the user, conventionally it would be /home/user/, where "user" is the user name can be anything like /home/binli.

"$" - is just a sign of the shell prompt, means that shell is ready to accept commands, you can understand it as a separator after which, you can interact with a shell. Can also be "#" which shows that **root** is the user who's session is going on.
```
binli@ubuntu:~$ sudo su -
[sudo] password for binli: 
root@ubuntu:~# 
```
## 4. ls command
**ls** is one of the  most used basic linux commands, used to **print** contents of a directory, by default it lists contents of current working directory(**pwd**).
```
binli@ubuntu:~$ ls
Desktop   Documents   Downloads
Pictures  Public      Videos
binli@ubuntu:~$ 
```
Example, use `ls /usr/bin` to list contents of the **/usr/bin** folder.
## 5. cd command
Assume you are in `/home/binli` directory, you want to go to the `/usr/local/share/fonts` directory, use `cd /usr/local/share/fonts`.
```
binli@ubuntu:~$ pwd
/home/binli
binli@ubuntu:~$ cd /usr/local/share/fonts
binli@ubuntu:~$ pwd
/usr/local/share/fonts
```
## 6. touch command
You can create a blank file with touch command. As example, use `touch hello_world.py` to create a blank `hello_world.py` file under the your home directory.
```
binli@ubuntu:~$ touch hello_world.py
binli@ubuntu:~$ ls
Desktop    Documents    Downloads  hello_world.py
Pictures   Public       Videos
```
## 7. mkdir command
The **mkdir** command creates new directories in your file system. 
Create a new directory called myfiles in the current directory.
```
binli@ubuntu:~$ mkdir myfiles
```
Creates the directory `/home/binli/linux/command/myfiles`. If any of the parent directories `/home/binli/linux` or `/home/binli/linux/command`, do not already exist, they will automatically be created.
```
binli@ubuntu:~$ mkdir -p /home/binli/linux/command/myfiles
```
## 8. chmod
The **chmod** command changes the permissions of files or directories. Only the file owner or a privileged user can change the access mode.
In general, chmod commands take the form:
```
binli@ubuntu:~$ chmod 755 hello_world.py
```
Here the digits 7, 5, and 4 each individually represent the permissions for the **user**, **group**, and **others**, in that order. Each digit is a combination of the numbers 4, 2, 1, and 0:   
4 stands for "read",  
2 stands for "write",  
1 stands for "execute", and  
0 stands for "no permission."  

## 9. cp command
You can copy files and directories with this command. Typical usage is like 
```
binli@ubuntu:~$ cp hello_world.py hello_world_copy.py
```
To copy a directory, including all its files and subdirectories, to another directory.
```
binli@ubuntu:~$ cp -r Documents Documents-copy
```
Also don't forget to use proper path when you are coping something to different location.

## 10. mv command
The **mv** command is used to move or rename directories and files.
```
binli@ubuntu:~$ mv hello_world.py rename_hello_world.py
binli@ubuntu:~$ mv Documents-copy rename_Documents
```
## 11. rm command
The **rm** command is used to remove directory or files.
```
binli@ubuntu:~$ rm rename_hello_world.py
binli@ubuntu:~$ rm -r rename_Documents
```




