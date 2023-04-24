# The Command Line

## What is it, how does it work and how do I get to one.

A command line or terminal is a text-based interface where users can enter commands by typing them on the keyboard and receive text feedback. On a Mac, the Terminal program can be found under Applications -> Utilities, or by using the key combination 'command + space' to bring up Spotlight and searching for Terminal. On Linux, it is typically located under Applications -> System or Applications -> Utilities, or by right-clicking on the desktop and selecting "Open in terminal." On Windows, if you plan to remotely log into another machine, you will need an SSH client such as Putty (which is free).

## An introduction to the Linux directory system and how to get around it.

In this section, we'll learn the basics of moving around the system

***pwd: which stands for Print Working Directory, It tells you what your current or present working directory is.***

`pdw`

***What's in Our Current Location?***

if want to know what is there in the directory

`ls`

***In order to move around in the system we use a command called cd which stands for change directory. It works as follows:***

`cd [location]`

If you run the command cd without any arguments then it will always take you back to your home directory.

`cd`

## Find out some interesting characteristics of files and directories in a Linux environment.

- In Linux, everything is treated as a file or directory.

- Files are identified by their names, which can be made up of letters, numbers, and special characters, and are often followed by a file extension indicating the type of file (e.g. .txt, .jpg, .html).

- Directories (or folders) are containers that can hold files and other directories.

- The root directory is the top-level directory in the file system, and all other directories and files are contained within it.

- Paths are used to specify the location of a file or directory in the file system, and can be either absolute (starting from the root directory) or relative (starting from the current working directory).

- The "dot" (.) and "dot-dot" (..) directories are shortcuts that allow you to refer to the current directory and its parent directory, respectively.

- File permissions specify who can read, write, and execute a file or directory, and can be viewed and modified using the ls and chmod commands.

- Hidden files and directories are those that are preceded by a dot (.) in their name, and are not normally displayed when listing the contents of a directory using the ls command.

- The file command can be used to determine the type of a file based on its contents, and can be useful when working with files that have unknown or incorrect extensions.

## Learn how to make the most of the Linux commands you are learning.

The manual pages are a set of pages that explain every command available on your system including what they do, the specifics of how you run them and what command line arguments they accept.

`man <command to look up>`

It is possible to do a keyword search on the Manual pages. This can be helpful if you're not quite sure of what command you may want to use but you know what you want to achieve.

`man -k <search term>`

Within a manual page, perform a search for 'term'

`/<term>`

After performing a search within a manual page, select the next found item.

`n`

## How to make, remove, rename, copy and move files and directories.

Make a directory

`mkdir`

Remove a directory

`rmdir <directory name>`

Create Blank File

`touch <file name>`

Copying Files or Directories

`cp <source> <destination>`

moving Files or Directories

`mv <source> <destination>`

Remove a file

`rm <file name>`

Remove a directory and all its contents

`rm -r <directory name>`

**NOTE: The Linux command line does not have an undo feature. Perform destructive actions carefully.**

## Cheat Sheet - A quick reference for the main points covered in this tutorial
[Cheat Sheet link](https://ryanstutorials.net/linuxtutorial/cheatsheet.php)