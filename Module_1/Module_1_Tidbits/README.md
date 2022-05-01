# Tools of the Trade - What I Use

The tools you use for programming come down to personal preference a lot. I've used a lot of different tools both in school, work, and personally. I'm gonna touch briefly here on some of the tools I've used, as well as what I currently use at work as well as what I'm using to make this project. All of this is just FYI, and I encourage you to explore and choose what fits you best.

There are actually two "main IDEs" I use, and one isn't exactly an IDE when you think about it...

## VSCode

When I first learned programming I worked with *Text Wrangler* and the terminal on an oldschool MacBook (the white plastic kind) using Python. Over the years I've used *Eclipse* to program Java, *Visual Studio* to work in C++, and a handful of other tools for different reasons. 

After I left school Microsoft elected to make a free, open source, multiplatform version of their IDE and named it *Visual Studio Code*. Part of why I've used *Visual Studio Code* is due to familiarity from *Visual Studio*. However the simplicity and extensibility of the tool is what has kept me with it. I know that whatever language and framework I'm using will have some level of support from the community. Its build in Git tools are incredibly useful as well.

## NeoVim + Terminal

I only use VSCode here and there though. Instead I live almost entirely in the terminal, whenever I can.

In college I took a few Linux specific courses that taught me the tools and concepts that have gotten me to where I am today, and what this project is based upon. My professor was very insistent on leveraging the command line whenever possible, and I'm glad that I fought through the learning curve to do that.

Vi is the default text editor on all Linux distros (when working from the CLI, that is). There are a few different flavors of it that have built upon it, including Vim and later NeoVim. There's a high learning curve to these programs because they take the same philosophies of programs like VSCode and crank the volume to 11. 

VSCode and similar tools focus on being simple first, and provide flexibility with plugins/extensions. Vi is the same, but even *more* simple. Vi looks at VSCode and says "mouse support? That's way too flowery and unnecessary."

Over the years I've used Vi, gotten frustrated with it, and then moved back to something like VSCode. Then some time passes and I think... "I'll give Vi a try again". Then I get frustrated again, and switch back. It wasn't until I got a job where I was programming all the time that I finally started using it heavily and finally got used to it. Part of getting through the learning curve is just practice, and if you don't get a lot of opportunity to practive then the learning curve never levels out.

As I mentioned before I choose to use the terminal for as much as possible. I realized that even running a Python script in VSCode just spits the results out into an embedded terminal. Why not cut out the middle man? Over time I've turned my terminal and NeoVim into a custom IDE that does exactly what I need, and cuts out all the unnecessary pieces.

It's also incredibly useful to touch the mouse as little as possible. You already know that using Alt/CMD + Tab is a hell of a lot faster than hunting for the program you want in the dock and switching to it. This extends to working in the terminal. I can write some code and run it without ever having to use the mouse or leave the keyboard. Even VSCode has an extension that provides keybindings similar to Vim.

There's one super important reason to why I use NeoVim though: Vi is on everything. Even if I'm doing the bulk of my work on a machine that I've setup myself, I still have to frequently connect to a headless server with nothing but the terminal. If I need to edit a text file there I HAVE to use Vi. If I use someone else's computer for whatever reason I may not know what software they use and in what configuration, but I *know* they have Vi. The Vi used on these machines are going to be minimal with none of the fluff I use day-to-day, but the keybindings and general flow are all the same.

### Making an IDE from the Terminal

I use NeoVim for the text editing side of things, but outside of that there are a lot tools that I use in the terminal for all the other things an IDE handles and then some. Even if you choose to use a GUI text editor, you can fill in the remaining gaps an IDE would have using various programs and tools all on the CLI. Here are some I use:

* TMUX: Let's me split my terminal into multiple windows. I can have my text editor and my CLI in two separate panels in a single window (just like in VSCode or another IDE).
* Ranger: This is a file explorer that runs on the command line. I get around my machine using mostly commands like `cd` and `ls`, but if I'm in a folder/project/repo I'm unfamilar with or need to comb through a bunch of stuff I'll use Ranger to give me a Finder like explorer I can navigate without needing a mouse.
* Navi: This is a "cheatsheet" application that let's me quickly look through the commands for a program and see what they do.
* Antigen and Oh-My-Zsh: These are theme and plugin managers for the terminal. They let me add color and formatting to my CLI, as well as extra "flavor" to make things easier like aliases and Git status info. An example of a few plugins I use:
	* zsh-syntax-highlighting: provides the same syntax highlighing an IDE does, but for all your BASH/Zsh commands.
	* zsh-autosuggestions: gives me autofill suggestions for commands, just like a web browser
	* web-search: I can type `google "what's that hipster song with the whistling"` and it will open my default browser with the search results
	* macos: I can control Apple Music and Spotify from the terminal, as well as launch macOS specific things when needed. For example I can type `ofd` and it will open whatever directory I'm in with Finder
	* Jump: this lets me mark directories and "jump" to them. Rather than typing `cd ~/Repos/Kickstart/Module_1` I can "mark" that directory and then jump to it like `jump M1`
* You can also write your own custom aliases and functions to accomplish whatever you need. I have a set of aliases all for Git that I use constantly. I don't need to type `git checkout -b sig` instead I can type `gcob sig`

All of these plugins and settings are contained in config files accross the system, and I use a program called Dotbot and a personal `.dotfiles` repo with all of my settings. If I move onto a new system I just clone that repo and run the install script, and everything needed is unpackaged and installed onto the system.

Theres an impressive number of things you can do in the terminal. If you wanna see some nerdy shit, go over to www.reddit.com/r/CommandLine and see some of the weird stuff you can do. You can even use the terminal as a web browser... which must be quite an experience.

# Odds and Ends

There are still some GUI applications I use here and there. Sometimes you just can't beat a good GUI, and sometimes it's really useful when you're learning.

These README files are written in Markdown, which is a markup language used all over the place to format text, typically on websites. I'm not a web dev, so the exact language isn't something I work with frequently enough to commit to memory. It's not complicated, but it's also not something I decided to bother with learning. So I'm using a program on my MacBook called *MacDown* to write and preview these files.

I actually like to use VSCode's Git integration when resolving more complex Git issues. I've found dedicated Git clients to be... not great. At least not the free ones. I use the command line version of Git almost exclusively, but sometimes there's a bunch of conflicts I need to comb through and resolve and it's just easier to do with a GUI. VSCode is fantastic for that.

While I don't personally use them, my coworkers often use some dedicated "diff" tools (and I just haven't gotten around to trying them out). You can use Git to see the "diff" (difference) between two files, as well as the same file accross two branches on a repo. But it's honestly hard to interpert on just the command line, since it's an inherently visual task. Kaleidescope is one such program I've seen being used.