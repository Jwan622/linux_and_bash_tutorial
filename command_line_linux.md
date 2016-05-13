The command line (i.e., all-text display mode) is a key part of any truly modern computer operating system1.

Because graphical user interfaces (GUIs) have become very easy to use in the past decade or so, it is no longer common for most computer users to utilize the command line, especially for simple tasks such as word processing, searching the web and sending e-mail. Thus, the command line is frequently perceived as being unnecessary, intimidating and even obsolete. A GUI is a display mode that contains images, windows and menus and which is manipulated primarily with a mouse.

However, the command line, also referred to as the shell (although the shell is actually a program the provides the command line), can be quite easy to learn and use, and its value soon becomes apparent after a little practice. Even a basic familiarity with it can make computers easier to use and facilitate performing tasks that might be difficult or impossible with a GUI. Such familiarity can also lead to an improved understanding of how computers actually work.

Many people who are new to the Linux command line will be familiar with the command line used in MS-DOS and think that the two are similar. However, the similarities are largely just superficial, and there are vast differences. The Linux command line is far more powerful (i.e., it is much more flexible and can do many more things), and in some ways it is much more user friendly.

Studying the Linux command line provides an education in much more than just how to use a specific operating system. One reason is that the Linux command line is virtually identical to the command line used on every other Unix-like operating system, e.g., Solaris, FreeBSD and Mac OS X. Thus, multiple operating systems are being learned simultaneously.

Studying the command line also provides insight into how computers really work. This is because the command line is much closer to the internal functioning of computers than are GUIs, which are generally just front ends for the commands used on the command line. Moreover, the underlying commands typically have greater flexibility than their GUI counterparts, they can easily be combined with other commands, and they can be used in situations where a GUI is not available (e.g., making system repairs) or is not functioning properly.


**The pwd Command**

A good first command to learn is pwd, which stands for present working directory. This command shows the name and location of the current directory, which is the directory (also called a folder on some operating systems) in which the user is currently working. All that is necessary in order to use this command is to type the word pwd in at the keyboard as follows and then press the ENTER key:

pwd

If the terminal window or console has just been opened, what will typically be shown on the next line on the monitor screen will be /home followed by another forward slash and then the name of the user's home directory (which is usually the same as the user name). For example, if the user has a user name of john, the line would say /home/john. This is because a user begins working at the command line in its home directory, home directories are located in the directory named /home, and a user's home directory typically has the same name as the user name.

Commands (and virtually everything else) in Unix-like operating systems are case sensitive, in contrast to MS-DOS, which is case insensitive. That is, lower case and upper case letters are treated as completely different characters. Thus, for example, pwd must always be written in all lower case letters, not as PWD or Pwd2.


**Command Options**

Many commands have numerous options, and ls is no exception. However, typically only a few of them are frequently used. Another commonly employed option for ls is -l, which provides a long listing, i.e., it provides much information about each object in addition to just its name. This additional information includes the type of object (e.g., file, directory or link), its permissions (i.e., who has access to it for reading, writing and/or executing), its owner (which is by default the same as its creator), and the date and time of creation.

When used together with both its -a and -l options, the command would be written as
```
ls -al
```



Like most commands, but unlike pwd, ls can accept input data, which is referred to as an argument. In the case of ls, arguments are the names of directories about which it is desired to obtain information. Any number of directories can be listed as arguments. They all follow ls and any options, and they are separated by at least one blank space.

For example, if it is desired to see the names of all the objects in both the directories /bin and /home, the following command would be used:

ls -a /bin /home

As is the case with /home, /bin is a standard first tier directory in the root directory, which is the single directory that contains all other directories and their subdirectories on a Unix-like operating system and which is represented by a forward slash ( / ). Like all other first-tier directories in the root directory, their names begin with a forward slash, in part so that they will not be confused with directories with similar names that are not first tier directories of the root directory.

The cd Command

The last of what are perhaps the three most basic commands on Unix-like operating systems is cd, which is used to change the current directory. This is equivalent to the CD and CHDIR commands in MS-DOS.

Thus, for example, to change the current directory to the /bin directory, the following would be used:

cd /bin

Likewise, to change to the root directory, the following would be used:

cd /

Any user can return to its home directory by using a tilde as the argument for cd. A tilde is a short, wavy, horizontal line that represents the home directory of the current user, and this character is located in the upper left hand corner on most standard English language keyboards. That is, any user can return immediately to its home directory by typing the following and then pressing the ENTER key:
```
cd ~
```
This is easier than typing the full name of the user's home directory as an argument, for example /home/josephine in the case of a user named josephine. It is just one of the numerous shortcuts that help make the command line on Unix-like operating systems so easy to use4.


Takeaway for me: / and ~ are two different directories. / is the root directory.
