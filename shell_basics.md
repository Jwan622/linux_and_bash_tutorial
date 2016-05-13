Shell scripts are short programs that are written in a shell programming language and interpreted by a shell process. They are extremely useful for automating tasks on Linux and other Unix-like operating systems.

A shell is a program that provides the traditional, text-only user interface for Unix-like operating systems. Its primary function is to read commands (i.e., instructions) that are typed into a console (i.e., an all-text display mode) or terminal window (i.e., all-text mode window) and then execute (i.e., run) them. The default shell on Linux is the very commonly used and highly versatile bash.

A programming language is a precise, artificial language that is used to write computer programs, which are sets of instructions that can be automatically translated (i.e., interpreted or compiled) into a form (i.e., machine language) that is directly understandable by a computer's central processing unit (CPU).

A feature of bash and other shells used on Unix-like operating systems is that each contains a built-in programming language, referred to as a shell programming language or shell scripting language, which is used to create shell scripts. Among the advantages of using shell scripts are that they can be very easy to create and that a large number are already available in books and on the Internet for use with or without modification for a wide variety of tasks. Shell scripts are also employed extensively in the default installations of Unix-like operating systems.


A First Script

The following example, although extremely simple, provides a useful introduction to creating and using shell scripts. The script clears the monitor screen of all previous lines and then writes the text Good morning, world. on it.

All that is necessary to create this script is to open a text editor (but not a word processor), such as gedit or vi, and type the following three lines exactly as shown on a new, blank page:
```bash
#!/bin/bash
clear
echo "Good morning, world."
```


After saving this plain text file, with a file name such as morning (or anything else desired), the script is complete and almost ready to run. Scripts are typically run by typing a dot, a forward slash and the file name (with no spaces in between) and then pressing the ENTER key. Thus, for example, if the above script were saved with the name morning, an attempt could be made to execute it by issuing the following command:
```
./morning
```


**How It Works**

The first of the three lines tells the operating system what shell to use to interpret the script and the location (i.e., absolute pathname) of the shell. The shell is bash, which is located in the /bin directory (as are all shells); thus the line contains /bin/bash. This instruction is always preceded by a pound sign and an exclamation mark in order to inform the operating system that it is providing the name and location of the shell (or other scripting language).

The second line tells the shell to issue the clear command. This is a very simple command that removes all previous commands and output from the console or terminal window in which the command was issued.

The third line tells the shell to write the phrase Good morning, world. on the screen. It uses the echo command, which instructs the shell to repeat whatever follows it. (The quotation marks are not necessary in this case; however, it is good programming practice to use them, and they can make a big difference in more advanced scripts.) In slightly more technical terms, Good morning, world. is an argument (i.e., input data) that is passed to the echo command.

As is the case with other commands used in shell scripts, clear and echo can also be used independently of scripts. Thus, for example, typing clear on the screen and pressing the ENTER key would remove all previous commands and output and just leave a command prompt for entering the next command.
