# Using Commands

## Choosing your shell

In most Linux systems, your default shell is the bash shell. To find out what your default login shell is, type the following commands:

```console
// show your username
$ who am i
hodung   ttys002  Jun  6 14:27
```

## Running commands

```console
// show the current day, month, date, time, timezone, and year
$ date
Wed Jun  6 14:31:10 JST 2018

$ pwd
/Users/hodung

$ hostname
Hos-MacBook-Air

$ ls
```

### Understanding command syntax

Most commands have one or more options you can add to change the command's behavior.

Options typically consist of a single letter, preceded by a hyphen.

However, you can group single-letter options together or precede each with a hyphen, to use more than one option at a time.

```console
// -l (long listing)
// -a (show hidden dot files)
// -t options (list by time)
$ ls -l -a -t
$ ls -lat
```

Some commands include options that are represented by a whole word. To tell a command to use a whole word as an option, you typically precede it with a double hyphen (--).

```console
$ ls --help
```


Many commands also accept arguments after certain options are entered or at the end of the entire command line. An argument is an extra piece of information, such as a filename, directory, username, device, or other item that tells the command what to act on.

``` console
$ cat /etc/passwd
```

Sometimes, an argument is associated with an option. Notice that the equal sign immediately follows the option (no space) and then the argument (again, no space).

```console
$ ls --hide=Desktop
```

Here’s an example of a single-letter option that is followed by an argument:

```console
// -c - create
// -f - file named backup.tar that includes all the contents of the /home/hodung directory and its subdirectories
// -v - show verbose messages
$ tar -cvf backup.tar /home/hodung
```

```console
\\ show all files and directories including hidden ones
$ ls -a
```

```console
\\ show the type of system you are running
$ uname
Linux

\\ also show see the hostname, kernel release, and kernel version.
$ uname -a
Linux nlfs-gw.local 3.10.0-862.3.2.el7.x86_64 #1 SMP Mon May 21 23:36:36 UTC 2018 x86_64 x86_64 x86_64 GNU/Linux
```

```console
$ date
Wed Jun  6 14:48:48 JST 2018

$ date +'%d/%m/%y'
06/06/18

$ date +'%A, %B %d, %Y'
Wednesday, June 06, 2018
```

To find out information about your identity, use the id command as follows:

```console
$ id
uid=1000(nlfs) gid=1000(nlfs) groups=1000(nlfs),983(docker)
```

You can see information about your current login session by using the who command.

```console
$ who -uH
NAME     LINE         TIME             IDLE          PID COMMENT
nlfs     pts/0        2018-06-06 14:37   .          5647 (172.16.102.221)
```

User nlfs is logged in on pts/0 (the virtual console on the monitor connect to the computer). The session began at 2018-06-06 14:37. The IDLE time shows how long the shell has been open without any command being typed (the dot indicates that it is currently active). PID shows the process ID of the user’s login shell. COMMENT would show the name of the remote computer the user had logged in from, if that user had logged in from another computer on the network, or the name of the local X display if that user were using a Terminal window (such as :0.0).

## Locating commands

Here is the order in which the shell checks for the commands you type:

- Aliases - Names set by the *alias* command that represent a particular command and a set of options. Type **alias** to see what aliases are set.
- Shell reserved word - Words reserved by the shell for special use. Many of these are words that you would use in programming-type functions such as *do*, *while*, *case*, and *else*.
- Function - This is a set of commands that are executed together within the current shell.
- Built-in command - This is a command built into the shell. As a result, there is no representation of the command in the filesystem. Some of the most common commands you will use are shell built-in commands, such as *cd* (to change directories), *echo* (to output text to the screen), *exit* (to exit from a shell), *fg* (to bring a command running in the background to the foreground), *history* (to see a list of commands that were previously run), *pwd* (to list the present working directory), *set* (to set shell options), and *type* (to show the location of a command).
- Filesystem command -  This command is stored in and executed from the computer’s filesystem. (These are the commands that are indicated by the value of the PATH variable.)

If a command is not in your PATH variable, you can use the locate command to try to find it. Using locate, you can search any part of the system that is accessible to you (some files are only accessible to the root user)

```console
$ locate chage
/usr/bin/chage
/usr/sbin/lchage
/usr/share/bash-completion/completions/chage
/usr/share/man/de/man1/chage.1.gz
/usr/share/man/fr/man1/chage.1.gz
/usr/share/man/it/man1/chage.1.gz
/usr/share/man/ja/man1/chage.1.gz
/usr/share/man/man1/chage.1.gz
/usr/share/man/man1/lchage.1.gz
/usr/share/man/pl/man1/chage.1.gz
/usr/share/man/ru/man1/chage.1.gz
/usr/share/man/sv/man1/chage.1.gz
/usr/share/man/tr/man1/chage.1.gz
/usr/share/man/zh_CN/man1/chage.1.gz
```
