# Module 1 - Tools of the Trade

The submodules for Module 1 are going to serve as the scaffolding for the rest of the project. There are a suite of different tools that are pretty ubiquitous in the field that they will explore, but what about the less ubiquitous ones? What about personal preference? What about options?

Before we get in to the types of tools we'll be using though...

## A Note on Naming Conventions

You may have noticed that some of the folders and other things in this repo are named a little odd. Like... why is this folder `Module_1` instead of `Module 1`. There are a few reasons for this, but the main reason is that programming (in general) reserves whitespace for things other than legibility. When you create a variable, function, etc it will always be a single, unbroken string. There will never be a variable named `foo bar`, instead you may see `fooBar` or `foo_bar`.

Each language has it's own naming conventions, like using certain formatting for variables depending on their scope (global/local/constant). You'll learn these as you learn that particular language, but there's one universal truth:

*Don't use spaces.*

Unless the text is something that is made purposely for humans (like a message appearing on the screen, or the title of a window), you should avoid spaces. **This includes folders and filenames**. Name your program `HelloWorld.py`  and not `Hello World.py`, you'll thank me later...

# Text Editors and IDEs

The vast majority of programming work is done either in a text editor, or in what's called an Integrated Development Enviornment. A text editor is self explanatory... but what's an IDE?

Text editors are used in programming typically as one half of a whole. You can write a program via a text editor but then... well... what do you do? The text editor can't really run it. Depending on the language and purpose of the program you may need to execute the file inside of the terminal, or compile it into binary code, or maybe it can only work when it's loaded onto a webserver. 

IDEs serve as a tool to marry the two software types together. They serve as a "one stop shop" to combine text editting with a collection of utilities to run your programs (and more). There are generally two types of IDEs: multipurpose, or single purpose. For example *Eclipse* is an IDE that is pretty much only used with the Java programming language. Similarly *PyCharm* is only used with Python. On the other hand an IDE like *Visual Studio Code* is used for a wide array of languages by leveraging plugins.

Regardless of the scope of an IDE, it provides a number of useful tools to a programmer such as...

* Syntax highlighting (the coloring of your code to help you visually structure/understand it)
* Code autocompletion
* Linting (the process of checking that your code is formatted correctly)
* Debugging tools such as breakpoints
* Built in code compilers or program shells
* A file explorer/workspace manager

Given all that information you may think "well why would I even use a text editor when I could use an IDE?" Great question! It all comes down to flexibility.

If we're just talking about using Notepad, then yeah... probably not a very useful tool compared to those previously listed. A text editor can still provide many of the same features as an IDE though! Syntax highlighting, code autocompletion, and linting are often provided by text editors. *Notepad++*, *BBEdit*, and *Text Wrangler* are all examples of text editors that offer these features. They don't typically offer the flexibility to run and debug your programs, but depending on the work you're doing you may not need that.

An IDE is often the most attractive option to new programmers because it seems to have all the features you want, and then some. They're great tools to use, but depending on what you're doing it may be like driving a Ferrari to McDonalds. There are some situations (and languages) that pretty much *require* an IDE (like *Swift* and its IDE *XCode*). Most of the time (particularly in this project) a good text editor combined with the terminal will be more than sufficient. 

Long story short: there are a lot of options here, and what you pick will mostly come down to the type of work you're doing as well as where/how you're doing it, and personal preference. I'll go over what I use (and for what) in the **Side Notes** section of Module 1. For now though, here are my recommendations for working with this repo.

## Recommended IDEs: Visual Studio Code

As I mentioned before, IDEs are robust tools with lots of features... but they sometimes have too many features, only support one or two languages, have licensing fees, etc. As I mentioned, there are some languages and types of work you'll want to use an IDE for, but the market for "free and flexible IDEs" is not as big as you would think.

[Visual Studio Code](https://code.visualstudio.com) is the only IDE I recommend for this project, as well as for beginners and people who need flexibility. The program is free and open source, and has a rich community of users and organizations developing extensions for it. Need a extension that lets you compile C# programs? How about one that lets you manage Docker containers? Or maybe you'd like something that gives you more control over how your Python scripts run? There are extensions for all of those things.

VSCode also comes with built in Git tools that are super useful. It provides custom themes, keyboard shortcuts, the list goes on...

## Recommended Text Editors - Atom, Sublime Text, and Vi

I've actually only used one of those three recommendations (Vi), but I'm still going to recommend [Sublime Text](https://www.sublimetext.com) and [Atom](https://atom.io) due to their ubiquity. Sublime Text is known pretty well for being the top dog when it comes to code editing... but you've gotta shell out $100 for it. 

Atom is open source, and is created by Github. Naturally it has some tight Git/Github integrations that are very attractive.

And then there's **Vi**... Vi is a whole other monster. I'm including it in my recommendations here because I genuinely do recommend it, but I don't really recommend you try using it right now...

It's arguably the most widely used text editor because it's installed on every Linux machine, as well as macOS (go ahead and open a terminal up and type `vi` if you'd like to see). It's a *CLI only* text editor, meaning you do everything inside the terminal without a GUI. It's got a pretty high learning curve, since there's no such thing as using your mouse to select where your cursor should be or selecting blocks of text. 

That being said, Vi (and it's derivatives, like Vim and NeoVim) takes the crown when it comes to speed, flexibility, and extensibility. The benefit of using such a "bare bones" program means you can tack on other plugins and programs to fit your needs. Additionally, since it's on literally every Linux machine you'll be able to use it whenever and wherever.

We'll go over Vi in it's own submodule later on, since you'll need to use it at least occasionally. You'll often end up using it when you're connecting to a remote server, or need to do a quick text edit without leaving the terminal.

# Git Clients

We'll go over the high level details of Git in 1.2, but I'll touch on client options briefly here. 

There's actually a number of options listed on [Git's own website](https://Git-scm.com/docs/Git-gui). Github also offers it's own [desktop client](https://desktop.Github.com), and as I mentioned above Git is often integrated in to other tools like VSCode and Atom. SourceTree and GitKraken are two common ones in use.

That being said, I recommend using Git from the terminal. Using a GUI Git client is very useful (especially those built in to editors), but I recommend using them as supplements to the CLI version of Git rather than a replacement.

# Other Tools for Another Time...

The programs covered here just scratch the surface of what you may use later on in your career. That being said, a good IDE/Text Editor and Git will serve as the bedrock you'll come to rest on. For now these are all you need to worry about, but there are some other programs and services you may come across on your journey. I won't be exploring any of them in this project, but feel free to read up on them if you so choose.

* Docker
* Kerberos
* Jenkins
* Circle CI
* Kubernetes