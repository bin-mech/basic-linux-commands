# basic linux commands 
## [What is the terminal?](https://itconnect.uw.edu/learn/workshops/online-tutorials/web-publishing/what-is-a-terminal/)
> **Terminals**, also known as command lines or consoles, allow us to accomplish and automate tasks on a computer without the > use of a graphical user interface. Using a terminal allows us to send simple text commands to our computer to do things like > navigate through a directory or copy a file, and form the basis for many more complex automations and programming skills. 

## 1. open a new terminal 
(1). *Open* the Dash by clicking the Ubuntu icon in the upper-left, type `terminal`, and select the Terminal application from the results that appear.

(2). Hit the keyboard *shortcut*: **Ctrl** + **Alt** + **T**
## 2. pwd command
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
## 3. ls command
**ls** is one of the  most used basic linux commands, used to **print** contents of a directory, by default it lists contents of current working directory(**pwd**).
```
binli@ubuntu:~$ ls
Desktop   Documents   Downloads
Pictures  Public      Videos
binli@ubuntu:~$ 
```
Example, use `ls /usr/bin` to list contents of the **/usr/bin** folder.
## 4. cd command
