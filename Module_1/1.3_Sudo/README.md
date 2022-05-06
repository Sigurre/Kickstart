# 1.3 Sudo Go Make Me a Sandwich

If you've spent any level of time looking in to programming or used Linux you're probably familiar with `sudo`. It's short for "Super User Do", and it allows you to exectute a command with elevated priveleges (similar to running a program as admin in Windows). Depending on the tasks you're using your machine for you may never have to use it, since it's really only used to make changes to protected files and subsystems.

`sudo` and `su` serve simlar functions: they allow the execution of a command with `root` priveleges, which is the account that has basically total control over the system. On some distros you can literally erase the entire filesystem if you're logged in as `root`, that's how powerful it is! You can use `su` to switch to `root`, but you'll very rarely end up using it.

Similarly `sudo` grants temporary `root` level priveleges to the currently logged in user account. As such it's much safer to use than `su`, since the eleveated permissions eventually expire. There is often some added protections for it as well, to prevent things like the aforementioned filesystem erasure.

## INFO: When and Why?

It may be tempting to just run all of your commands as `root` or with `sudo`, but there are a plethora of reasons to avoid it. Security and useability are pretty high on that list, but it's also useful to keep in mind that you'll often be working with multiple machines via the shell in your day-to-day work. Regardless of what you choose to do on your local machine, you'll need to adhere to the standards and practices used on all of the machines you will be interacting with.

As such, it's best to try and limit your use of `sudo` when programming and configuring things. There isn't a need to avoid it, but be aware of when it's appropriate to use it. The primary "gotcha" that you can run in to is when setting up some sort of automation, or installing a program. Depending on the OS you're using it's possible to install a program via `sudo` and then you're never able to use it *without* invoking `sudo`. That can be inconvenient, but it can also cause other file permission issues when automating. If you write a script that needs to be able to run with little interaction on multiple systems you don't want to be fighting with `sudo` requirements. Down that road leads madness...

It should be noted that the distro you're using may require `sudo` in order to install *anything*, while others won't even bat an eyelash. MacOS in particular doesn't typically require any kind of `sudo` priveleges when installing things via `brew`, but the distro you're using may require it. When in doubt, try it *without* `sudo`. If it doesn't work you can type `sudo !!` to run the command again with `sudo` permissions.

## INFO: Permissions, chown, and chmod

It's important to be mindful of the permissions and ownership of any files you're working with. You typically want a script to function with minimal intervention from the user, and without godlike abilities. Limiting the scope of your automations will reduce security vulnerabilities, simplify maintenance, and ensure stability. There are times when you'll want a script to run as `root`, but if it doesn't *need* to be run as `root` then it *shouldn't* be run as `root`.

There are two important concepts when it comes to file permissions: mode and ownership. In the simplest terms, ownership is *who owns* and can work with the file and mode is *what can be done* with the file. A user may be the owner of a file, and can read it and write to it, but they may not be able to execute it. There are a lot of complexities that can arise from these structures, and you'll get more comfortable with them as you gain hands on knowledge.

# TASK

Just one task to do this time!

* Create a file that is owned by `root`
* Now change the ownership to your current user
* Make the file readable and writeable
* Now make the file readable and executable, but not writeable

# Resources

Info on [chmod](https://www.computerhope.com/unix/uchmod.htm) and info on [chown](https://www.computerhope.com/unix/uchown.htm). Also checkout their `man` pages!

A nice writeup on the use of `sudo` can be found [here](https://www.beyondtrust.com/blog/entry/unix-linux-privileged-management-should-you-sudo).
