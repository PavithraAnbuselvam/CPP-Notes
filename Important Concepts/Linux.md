Linux:

Linux is a Unix-based open-source operating system.The primary goal of Linux was to give a 
free and low cost operating system for people who couldn't buy windows,ios or unix.

Linux Kernal:

The Linux Kernal is a low-level software system.It is used to keep track of resources and
give a user interface.

Components of Linux:

Shell- It is a Linux interpreter which is used for executing commands.

Kernal- Kernal is the core part of the operating system which is used to manage hardware and
operations.

Which shells are used in Linux?

fish-Friendly Interactive Shell offers some special features such as web-based configuration.

bash- Bourne Again Shell is the default for most of the Linux distributions.

zsh- Z Shell offers unique features like startup files, filename generation, login or 
logout watching, and closing commands.

csh - C Shell follows C like syntax and has features like spelling correction as well as
Job Control.

Swap Space:
Swap Space is the extra space utilized by Linux to temporarily keep concurrently running 
processes when RAM space is insufficient.When you start a program, it is stored in RAM so that the
CPU can quickly retrieve data.Swap Space is used in the form of an extension of RAM by Linux.

File permission in Linux:
Read- allows users to open and read the file.
Write- It allows its users to open and edit the file.
Execute- It allows its users to run the file.

inode:
It is a unique name provided by the operating system for each file.

process id:
process id is also a unique id provided to each process.

Linux directory Commands:
pwd- displays path of the present working directory.
is-Lists all the directories and files in the present working directory.
cd- It is used for changing the present working directory.
rmdir- It deletes a directory.
mkdir- It is used to create a new directory.

Various process states in Linux:

Ready-The process is ready to run.
Running- The process has been executed.
Wait or Blocked- The process is waiting for the input.
Completed or terminated- The process completed execution or was terminated by the system.
Zombie- The process terminated but the information is still available in the process table.

Process Management System Calls:

fork()-It is used for creating a new process.
exec()-It is used for executing a new program.
wait()-Wait until the process completes the execution.
exit()-It is used to exit from the process.
getpid()-Get the unique process id of the process.
getppid()-Get the parent process unique id.

Redirection Operator:
The redirection operator is used for redirecting the output
of a specific command as an input to another command.
Two ways-
1)'>' overwrites the files's existing content or creates a new one.
2)'>>' adds new content to the end of an existing file or creates a new one.

Latch:

A Latch is a temporary storage device that is controlled by a timing signal
which can either store 0 or 1. A latch is primarily used to retain state information
and has two stable states (high output or 1 and low output or 0).

To rename a file in Linux:

There is no particular command for that,but we can use the copy or 
move command to rename a file.

->Move command - $ mv<oldname> <newname>
->Copy command - $ cp<oldname> <newname>
->Delete command -$ rm<oldname>

To write the output of a command to a file:

You must use the redirection operator (>) to do this.
Syntax: $ (command) > (filename)

To copy files to aFloppy Disk:

->Mount the floppy disk.
->Copy the files.
->Unmount the floppy disk.

To identify which shell you are using:

Open the terminal and run: $ echo $SHELL

To sort the entries in a text file in ascending order:

$ sort sample.txt

Linux Commands:

1)ssh-"SSH" stands for Secure Shell,a network protocol that provides 
a secure way to access and manage remote computers over an unsecured network.

ssh username@hostname

copy files with scp:scp file.txt username@hostname:/remote/directory/

2)ls -  Lists files and directories in the current directory.

3)pwd - print working directory.

4)cd -change directory

5)touch - to create empty files or update the timestamp of existing files.

6)echo - to display a line of text or a variable value to the terminal.

7)nano - terminal-based text editor in Unix/Linux. It's beginner-friendly 
and used to create or edit files directly from the command line.

nano filename.txt to open

| Shortcut   | Action                             |
| ---------- | ---------------------------------- |
| `Ctrl + O` | Write/save file ("O" for Output)   |
| `Ctrl + X` | Exit nano                          |
| `Ctrl + K` | Cut current line                   |
| `Ctrl + U` | Paste the cut line                 |
| `Ctrl + W` | Search within the file             |
| `Ctrl + G` | Help (shows all commands)          |
| `Ctrl + C` | Show cursor position (line/column) |

8)vim - widely-used text editor in Unix/Linux systems.

Enter Insert mode to start typing:
Press i → now you can type.

Exit Insert mode:
Press Esc

Save and Exit:
Type :wq → save and quit
:q! → quit without saving
:w → save only

9)cat -to display, create, and concatenate files

10)shred -  to securely delete files by 
overwriting their contents multiple times, making data recovery extremely difficult.

11)mkdir - to create directories (folders).

12)cp - is used to copy files and directories.

13)rm - to remove (delete) files or directories.

14)rmdir - is used to remove empty directories only.

15)ln -to create links between files — either hard links or symbolic (soft) links.

16)clear -to clear the terminal screen.

17)whoami -it prints the current logged-in username.

18)useradd -to create a new user account.
sudo useradd [options] username

19)sudo -allows a regular user to run commands with superuser (root) privileges, 
as long as they are permitted to do so.

| Command                | Description                          |
| ---------------------- | ------------------------------------ |
| `sudo useradd newuser` | Add a new user                       |
| `sudo passwd username` | Set/change password for another user |
| `sudo apt install vim` | Install software (Debian/Ubuntu)     |
| `sudo reboot`          | Reboot the system                    |
| `sudo nano /etc/hosts` | Edit system files                    |

20)adduser - Creates the user

21)su - to switch user accounts — most commonly to become the superuser (root).

22)exit - exit the current session.

23)passwd -

24)apt -to install, update, upgrade, and manage software.

25)finger - to display information about system users

26)top -shows a real-time view of system processes, CPU usage,
memory, and more. It’s like Task Manager in the terminal.

27)kill - to terminate processes manually by sending them signals (usually SIGTERM or SIGKILL).
kill [options] PID

28)to kill processes by name, instead of needing the exact process ID (PID).
pkill [options] process_name

29) systemctl -to control and manage systemd services in Linux systems that use 
systemd (like Ubuntu, Debian, CentOS, Fedora, etc.).

30)df - to display disk space usage of mounted file systems.

31)ps - to display information about running processes on your system.
to compress files and directories into a .zip archive.
zip myfile.zip file.txt


man

whatis

curl

zip
unzip
less
head
tail
cmp
diff
sort
find
chmod
chown
ifconfig
ip address
grep
awk
resolvectl status
ping
netstat
ss
iptables
ufw
uname
neofetch
cal
free
df
ps

htop
kill
pkill
systemctl
history
reboot
shutdown













