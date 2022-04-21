# Kickstart - A Simple Guide to the LAMP Stack

We live in a time where anyone can learn how to code... kinda. There's no end to the variety of tutorials and certificates online, but it's easy to get lost and wonder **"Am I learning the right things?"** or **"do I really have to do every little step in this tutorial?"**

This repository serves as a framework for getting started with programming in a practical way, while keeping the hand-holding to a minimum. 

Want to cut to the chase? Skip to the **"Get started"** section at the bottom!

**Please note that this whole project is a WIP, and will be added to and reorganized as it grows.**

## Who is this for?

The aim of this guide is to expose you to the concepts and tools that are most commonly used in a variety of software development and IT fields, as well as point towards resources that you can leverage to both learn and lean upon.

As such, there are a few things that you'll want to be familiar with before jumping in. Keep in mind that only shallow understanding of these subjects are needed--you don't need to be able to explain them, just that you know they exist! All of these subjects will be explored in a combination of resources, tutorials, and mini projects.

* Basic Linux and/or macOS knowledge
* That programs are made of loops, variables, and other logical structures
* Databases and computer networking concepts
* The server/client relationship
* The CLI (Command Line Interface), commonly referred to as Terminal on macOS (and many Linux Distros).
	* BASH or ZSH are the "Shells" used by these interfaces, but we'll cover that later...

**_It should also be noted that this guide is a Linux/macOS only guide, and Windows concepts will not be covered._**

## How it's structured

In this repository (repo for short) is a collection of folders and files that serve as the structure of the "curriculum". I will be referring to the top level directories as "modules", while the folders nested within them are "submodules" _They are organized in such a way to build upon eachother in succession, but you can work with them at your own pace and in whatever order you would like._ You may find that there are sections that you feel familair and confident with, and want to skip over. Or maybe there's a module that is particularly difficult or confusing, but you don't want to get hung up on it. Feel free to skip ahead and come back later! There are a few caveats though:

* There are some modules (or submodules) that I will mark as **critical**. These are ones that I consider paramount to understanding the concepts of this tutorial, and should not be *completely* skipped.
* The entire structure of this tutorial relies on the concepts in Module 1.1 and 1.2, *and I highly recommend completing them before moving on to the next one.*
* "Completion" is a loose term here, and can vary depending on your comfort level. While there are some goals that will be stated in each module, there's no checklist you need to go through. Move on when you feel ready, and feel free to reach out if you have questions or want a subject expanded on.

Finally, there are a few important notes about the project:

* This project works on the honor system, in a sense. You don't need to "submit" any work you complete if you don't want to. I'm serving as a mentor, not as your professor.
	* The one exception to this is Module 1.2, because it involves working with this repo and pushing changes to it.
	* You'll be pushing your work to your own personal branch on Github (see Module 1.2) for consistency and practice, but I won't critique your work unless requested.
	* If you want help with something, want something expanded upon, or want critique of your work you will do so via GIT and Github (see Module 1.2--seriously, it's an important module).
* Most modules will be split in to an **Info** section, a **Prompt** section, and a **Resources** section.
	* The **Info** section will include my personal thoughts on the subject(s) covered in the module.
	* The **Prompt** sections will outline the project, task, or concept that is to be explored.
	* The **Resources** sections will include tutorials and documentation to help you learn how to address the Prompt.
* I will provide hints and other thoughts in the **Resources** section. I do recommend looking at the information I include here, but try saving it for when you get stuck or have completed the associated Prompt!
* Whenever a **Prompt** requires you to make files/code/folders do so inside of the (sub)module the **Prompt** is located (which will be in the `README.md` file for that folder).

**FINALLY** it should be noted that you can follow this guide directly through your web browser in Github, or by opening the Markdown files (denoted by the `.md` extension, just like this README!) on your local machine in the editor of your choice.

## Get Started

Enough is enough! Let's get started! In order to begin you'll need to clone this repo to your local machine, and in order to do so you'll need [GIT](https://git-scm.com/). I'll go over details of GIT in Module 1.2, but for now you can install it using one of the following methods:

* [Recommended] Download and install it from the CLI using the [package manager for your Distro](https://git-scm.com/download/linux), or [Homebrew](https://git-scm.com/download/mac) for macOS.
* Download it from the [GIT website](https://git-scm.com/downloads).

Once you've downloaded and installed GIT we'll need to setup your credentials with GIT and Github, then clone the Kickstart repo. There's multiple ways to do it (some easier than others), and some are preferable. However you choose to do it is up to you, but I recommend setting up SSH authentication to work with Github since that's what most companies use, but it's not a very beginner friendly method. Use whatever method works best for you currently. You can always set up SSH authentication later.

Follow Github's docs on [setting up your credentials](https://docs.github.com/en/get-started/getting-started-with-git/setting-your-username-in-git). Also take a look at their [Getting Started with Git](https://docs.github.com/en/get-started/getting-started-with-git) documentation for general guidance on how to set everything up. 

All of my examples in this project will be using the Terminal, but however you accomplish the task at hand is up to you. If you're cloning the repo via CLI then open your terminal and change to the directory where you want to keep it. I will be using the home directory (denoted by `~` in BASH and ZSH) in all my examples for simplicity. Personally I usually have a `Repos` folder in my home directory where I keep all my projects, and will be using that as an example this time.

1. Change to the desired directory with `cd` (change directory). Typing `cd` in the terminal on its own will take you to the home directory
2. Clone the repo with `git clone git@github.com:Sigurre/Kickstart.git` or `git clone https://github.com/Sigurre/Kickstart.git`

Example output:
```
cd Repos
git clone git@github.com:Sigurre/Kickstart.git
Cloning into 'Kickstart'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
```

Now open Module 1 and we'll get started!