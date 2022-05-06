# 1.1 Tidbits

As promised, here are some hints and thoughts on the Tasks for Module 1.1! I do recommend trying to complete these tasks on your own first, but there's no shame in needing some direction!

## TASK 1

This task involves navigation of the filesystem using the command line, and only uses a few commands to accomplish it. These are gonna be your best friend as you go along.

* `cd` is the command used to "change directories". You can either provide a full path, or a relative path. Additionally you can type `cd` with no arguments to immediately jump to your home directory `~`
* `ls` is used to "list" what's in your current directory (when provided no arguments). You can also provide an absolute or relative path to list what's in a directory without changing to it
* Simply enough `clear` is the command to clear the terminal screen so there's nothing on it. I typically setup an alias so I can type `clr` instead
* You can provide additional arguments to `ls` to change how info is output. In this case we can add the `-l` (lowercase "ell") to the command to print everything out in "long format": `ls -l`
	* You can refer to the `man` page for more info, but the most useful info you can get from this argument is the date/time, size, and who owns the file
	* It's worth noting that the size is listed in bytes, which isn't always useful. You can have `ls` print them in "human readable" format with `-h`
	* You can also use the `-a` argument to include hidden files (those prepended by a `.`)
	* You can combine these to show *everything* in a directory and their details in a human readable format: `ls -lah`
* `pwd` stands for "print working directory", and prints the entire path of your current directory to the terminal
* Finally, you can dump the contents of a file directly to the terminal using `cat`. This may not seem useful at first, but it's incredibly powerful when combined with other commands via a pipe `|`

You might wonder what the `/bin` directory is. This is the directory that contains the binary files for the various commands you've been using. Other notable directories in the root are `/opt` and `/tmp`, and I recommend reading up on them.

## Task 2

* The command to create a new file is `touch` (idk why). In this case you would run `touch HelloWorld.txt`
* Creating a new directory is done with `mkdir` (make directory), using either an absolute pathname or a relative one (I'm sure you're noticing a pattern here...)
* Use the `mv` (move) command to migrate a file to a different location. `mv FileName ~/NewFileLocation`
	* Oddly, this is also how you *rename* a file! You're "moving" the file from one name to another: `mv FileName FileName2`
* You can use `cp` to copy a file. It should be noted that you need to provide a target directory *or* a target filename
* Hidden files are prepended by a period: `.`. Simply adding a period to the beginning of a file or directory name will hide it. This will hide it from `ls` unless you add the `-h` argument
* You can use `rm` (remove) to delete a file. Additionally you can use `rmdir` to remove a directory (if it's empty)
	* Removing a non-empty directory can only be done using the `-r` for `rm` argument to make the function recursive. `rmdir` does not provide the same functionality

## Task 3

This is where we start combining commands and functions together.

* You can use `ls` to print the directory, then append it to a file with a `>` or `>>`. The former creates the file if it doesn't exist, or overwrites it if it does. `>>` does the same, but appends rather than overwriting.

`ls /bin > output.txt`

* We can utilize the `cat` command from before to spit the contents of our file to the terminal, then pipe that to a command that we can use to search for our desired string.

`cat output.txt | grep "sleep"`

## Odds and Ends

Getting around the filesystem is the most important and most commmonly used collection of features you'll use. As such keep a few of these tips in mind:

* The tilde `~` is shorthand for your home directory. When providing absolute file paths you can leverage this to your benefit. `~Kickstart/Module_1/1.1_LAMP` is a lot easier to type than `/Users/sigurre/Kickstart/Module_1/1.1_LAMP`
* As mentioned above, using `cd` with no arguments takes you straight to your home directory
* The shell interperts the "current directory" and the "parent directory" as `.` and `..` respectively (not to be confused with a period to hide a file). You can leverage this to go up one directory: `cd ..`. You can also use it to provide relative paths to commands, eg: `cat ./SomeDir` although this is less common. When running a script from your current directory it needs to use the `.` in the file path: `./someScript.sh`
