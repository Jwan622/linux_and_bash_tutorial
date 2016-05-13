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



**The touch Command**

The touch command is the easiest way to create new, empty files. Its syntax is

touch [option] file_name(s)

No options are required for basic file creation. Thus, for example, to create a new file named file1 within the current directory (i.e., the directory in which the user is currently working), all that is necessary is to type the following command and then press the ENTER key:
```
touch file1
```


**The rm command**

And the following would remove everything in the directory dir1:
```
rm dir1/*
```

As another illustration of the great versatility that wildcards add to the command line, the following would delete all files in the current directory that have a file name extension of .html but would leave all others intact:
```
rm *.html
```


As a safety measure, rm does not delete directories by default. This is important because once deleted, it is extremely difficult or impossible to recover deleted data on Unix-like operating systems (in contrast to the Microsoft Windows operating systems). In order to delete directories, it is necessary to use the -r option or the -R option (they are the same). This option recursively removes directories, along with all of their contents, that are included in the argument list; that is, the specified directories will first be emptied of any subdirectories (including their subdirectories and files, etc.) and files and then removed.


**The cp Command**

The cp command is used to copy files and directories. The copies become independent of the originals (i.e., a subsequent change in one will not affect the other).

cp's basic syntax is
```
cp [options] name new_name
```
If a file with the same name as that assigned to the copy of a file (or a directory with the same name as that assigned to the copy of a directory) already exists, it will be overwritten. By default, cp only copies files and not directories.

When a copy is made of a file or directory, the copy must have a different name than the original if it is to be placed in the same directory as the original. However, the copy can have the same name if it is made in a different directory. Thus, for example, a file named file4 which resides in the current directory could be copied with the same name into another directory, such as into /home/john/, as follows:

cp file4 /home/john/file4



Any number of files can be simultaneously copied into another directory by listing their names followed by the name of the directory. cp is an intelligent command and knows to do this when only the final argument is a directory. The files copied into the directory will all have the same names as the originals. Thus, for example, the following would copy the files named file5, file6 and file7 into a directory named dir6:
```
cp file5 file6 file7 dir6
```


cp's -r option, which can also be written with an upper case -R, allows directories including all of their contents to be copied. Thus, for example, the following command would make a copy of an existing directory called dir7, inclusive of all it contents (i.e., files, subdirectories, their subdirectories, etc.), called dir8:
```
cp -r dir7 dir8
```



**The mv Command**

The mv command is used to rename and move files and directories. Its basic syntax is:
```
mv [options] source target
```
If the target file or directory is located in the same directory as the source file or directory, then the source file or directory can only be renamed. If both are in different directories, then the source file or directory is moved to a new directory, in which it can keep its original name or be assigned a new name.

Thus, for example, to rename a file called file8 to file9, both in the current directory, the following would be used:
```bash
mv file8 file9
```
The following would move a file named file10, without changing its name, from the current directory to an existing subdirectory of the current directory named dir9:
```
mv file10 dir9/file10
```
Detailed information (including all options) about mv as well as all of the other commands discussed above can be obtained by using their **--help option**. Thus, for example, to obtain more information about the mv command, the following would be used:
```
mv --help
```
