# Module 1.1 - The LAMP Stack

LAMP Stack might be a bit of a dated term, but it still captures the ideas that build the modern technological world. Depending on who you ask LAMP may stand for a few different things, but they're typically one of the following:

L - Linux

A - Apache

M - MariaDB or MySQL

P - PHP, Perl, or Python

**Linux** serves as the foundational OS for the server/client infrastructure that makes up the web. Almost all servers--whether they be a webserver for a Fortune 500 company, or a the file server in an office--run on Linux. It serves as a host for the other items in the stack...

**Apache** is the software foundation behind the modern web. Apache HTTP Server serves as the backbone for most webservers Other software tools have broken in to the field, but Apache servers running on Linux machines are still used globally.

**MariaDB** and the newer/more popular **MySQL** (a version of SQL) are the database engines that fuel the world. From the storage of user information for websites to inventory lists in a warehouse, these database services running on Linux machines to fuel the other services with data. There are many different database tools now in use (usually some form of SQL), but MariaDB was arguably the first on the field followed closely by MySQL. Also they're the only ones that fit the acronym...

**PHP** and **Perl** were the most common scripting languages of the early web. Much of the logic behind web forums and other web tools were handled by these languages. They served as the string that tied the other pieces of the LAMP Stack together. They have since fallen off in useage sharply in favor of **Python**, but they're still used from time to time.

This project is not concerned with the web development side of things though, so we'll only be focusing on the L and the P (Linux and Python, in this case). It's useful to know the other components of the stack though, because it provides context to how everything fits together.

## INFO: The ABCs of NIX

This project assumes you know your way around Linux and its Distros, but there are some important features of the OS that are important to know from front to back. Linux and macOS share a common ancestor: UNIX, which was one of the first operating systems used in modern computing and was made alongside the C programming language. As such, both the OSes share some common features and are sometimes referred to as *NIX operating systems, but there are some small quirks between the two we'll cover later.

All NIX OSes are built upon a type of "shell". There's a bit too much to expand on here, but know that if you've ever run `apt get` to update Ubuntu you're interacting with a shell. The most commonly used shell is the Bourne Again Shell (`BASH`) and is the default on most Linux Distros. It was also the default shell on macOS until Catalina, when it was replaced with the Z Shell (`Zsh`). Both of them function mostly the same, since `Zsh` is simply an extension of `BASH`.

These shells serve as the basis of how every NIX OS functions. While they are technically nothing more than a text box that accepts typed commands, most (if not all) basic functions rely on them. Even interracting with a GUI is just interfacing with the same commands used by the shell. Moving a file, adding and saving text, connecting to a wifi network--they all leverage the same structures.

### Leaning on shells

Working in most technical fields (*especially* fields like IT and DevOps) hinge upon proficiency in working with a shell. While there are a suite of graphical tools that can help you accomplish your goals, using a shell whenever you can will make your life easier. This is especially true when interacting with remote servers that are "headless" (meaning they have no monitor, or sometimes even no GPU). Editing a text file using a code editor/IDE is great, but when you need to edit a text file on a machine that you can *only* connect to via SSH in a Terminal window you don't want to be left clueless.

Throughout this project I encourage you to leverage your shell wherever possible. **_This is especially true for file management._** Using GIT from the shell is also useful, and using a shell based text editor like VIM, NeoVIM, or nano for basic tasks are invaluable. You're welcome to use whatever tools you'd like, but sometimes simpler is better.

Most of my work is done from my Terminal and a web browser. As such almost all of my examples and instructions will be built with a shell in mind. GUI tools are an attractive option to default to, and while I don't necessarily discourage it I do recommend being familiar with their shell equivalents. If you're more comfortable moving files in Finder, or editing your code in VSCode, that's totally fine. But you should know how to accomplish the very basics of each of those applications via the Terminal.

## INFO: Monty Python's Favorite Programming Language

Python (which is actually named after Monty Python, funny enough) is an incredibly robust and flexible programming language. It has exploded in popularity, and is used widely across various fields. We'll be using Python in this project due to its prevalence, as well as its simplicity. Python comes pre-installed on macOS and most Linux Distros. We'll be using **Python 3.8+** in particular. 

### Which programming language is best?

One common pitfall I encountered when I first started learning programming and IT concepts was wondering "am I learning the right thing?" This was especially true when it comes to programming languages. When you first start off learning a language you'll quickly hear the pros and cons of using it for X and Y. The truth is: it doesn't really matter what language you learn with.

You'll learn to use a number of different languages over the course of your career. Some languages are easier to use or learn than others, and some are very well suited to certain tasks but are obscure and hard to use. The foundational information is what's important though. If you know the basics to write a program in one language, you can learn how to write the same thing in a different language easier than you may think. The internal mechanisms and logical structures between them stay the same.

## INFO: The Task at Hand

The primary focus of this submodule is to ensure that you're comfortable with using the CLI for basic tasks. Working in tech means reading a lot of raw text data, and typing a lot of commands...

Before providing the Prompts, here are a few key shell concepts that will help contextualize things. 

* All commands you invoke on a CLI are actually programs being run from a file somewhere on the machine. Even the most basic commands like `ls` (lists items in a directory) or `cd` (change directory) are programs.
* Most commands accept one or more "arguments" when you invoke them. Depending on the purpose of the command they may be preceeded with one or two dashes (`-` or `--`), or they may just be standalone. 
	* Using `ls` as an example, we can run the program with the `-S` argument to sort the output by size (largest to smallest): `ls -S`
* The output of one command can be fed in to the input of another one via "piping". Ths is done with the pipe `|` symbol. 
	* This lets you chain the function of one program with another, like using `cat` to print the contents of a file to the shell, then "piping" it to the `grep` program to search for a particular word: `cat HelloWorld.txt | grep "world"`
* You can find more info on a command by checking its "man" page, or using the `--help` argument if the program has one. The man page (short for manual) can be accessed by prepending `man` to the command. For example, to see the man page for `ls` you would run `man ls`. To see the help page for `git` run `git --help`. 

Lastly here are the skills that you should be able to perform comfortable via a CLI in order to be succesful:

* Navigate a directory tree
* Move, copy, create, and delete files/folders
* View information about a machine's disk usage
* View information about a machine's CPU/RAM/etc useage
* Connect to another computer to transfer files (like SCP), or interact with it's shell (SSH). NOTE: This may be covered in a later module, I'm undecided. :p
* Pipe the output of one command in to another, or in to/out of a file
* Install, uninstall, and update programs and packages
* Understand how and when to use `sudo`
* Basic text editing

TODO: "Nice to have"

# Prompts - CRITICAL

These prompts will focus on using the CLI to accomplish certain tasks. As such, they are **critical** and should be done before moving on. Don't skip them unless you know you can do them easily!

## PROMPT 1

## PROMPT 2

## PROMPT 3

## PROMPT 4

# Resources

There are so many tutorials and guides on using BASH and its kin out there. I'll list some of them, but most of what you find googling will probably be sufficient. Personal preference is the biggest factor here. A lot of learning BASH will involve googling something when you hit a wall, but there's a rule of thumb I like to follow:

1. Check the `man` or `--help` page first. There may be an argument or other quirk you overlooked
2. Most tasks can be accomplished with an already existing command on your system. Googling can help you determine the best one for the task
3. Keep things simple, but not too simple. Sure you might be able to accomplish the task using a single command, or you could do the same thing with 11 commands all piping to each other. But maybe the solution with 3 commands piping to each other is the best one?
4. Tutorials on a program or concept are often more useful than someone outright providing an answer on StackOverflow. It helps to know the basic concepts more than the utilization of those concepts.

## Tutorials

A great place to start finding tutorials: [13 resources for learning to write better Bash code](https://www.redhat.com/sysadmin/learn-bash-scripting)

[Bash Guide for Beginners](https://tldp.org/LDP/Bash-Beginners-Guide/html/)

[Getting started with Bash](https://riptutorial.com/bash)

[Bash Scripting Tutorial for Beginners](https://linuxconfig.org/bash-scripting-tutorial-for-beginners)
