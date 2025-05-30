# Task 1 Introduction 
Linux is just another operating system like Windows, iOS and MacOS, and one of the most popular in the world powering smart cars, android devices, supercomputers, home appliances, enterpise servers, and more.

We'll be covering some of the history behind Linux and then eventually starting your journey of being a Linux-wizard! Thsi room will have you:
- Running your very first commands in an interactive Linux machine in your browser
- Teaching you some essential commands used to interact with the file system
- Demonstrate how you can search for files and introduce shell operators

# Task 2 A Bit of Background on Linux

## What is Linux?

Linux is a free, open-source, Unix-like operating system. While often used via the command line, it also supports graphical interfaces. Many operating systems are based on Linux.

## Where is Linux Used?

It's fair to say that Linux is far harder to approach than Operating System's such as Windows. Both variants have their own advantages and disadvantages. For example, Linux is considerably much more lightweight and you'd suprised to know that there's good chance you've used Linux in some form or another every day.

Linux powers things such as:
- Websites that you visit
- Car entertainment/control panels
- Point of Sale (PoS) system such as checkout tills and registers in shops
- Critical infrastructures such as traffic light controllers or industrial sensors


## Flavours of Linux

The name "Linux" is actually an umbrella term for multiple OS's that are based on UNIX (another OS). Thanks to Linux being open-source, variants of Linux come in all shapes and sizes - suited best for what the the system is being used for.

For example, Ubuntu & Debian are some of the more common distributions of Linux, because it is so extensible. You can run Ubuntu as a server, or a fully-fledged desktop. We're going to be using Ubuntu.

- Ubuntu server can run on systems with only 512MB of RAM!

Similar to how you have different versions Windows, there are many different versions/distributions ("distros") of Linux.

# Task 3 Interacting With Your First Linux Machine (In-Browser)

In this section, I started my Ubuntu Linux machine via a web browser. After deploying the machine, I found the following information at the top of the website:

- Active Machine status
- IP address
- timer
- Buttons to manage the machine (e.g., ?, Add 1 hour, Terminate)

I was able to interact with the machine directly in the browser using a terminal interface, similar to how I would use SSH on a remote server.

# Task 4 Running Your First few Commands

A large selling point of using OS such as Ubuntu is how lightweight it can be. This doesn't come without the disadvantages, where for example, often there is no GUI, or what is also known as a desktop environment that we can use to interact with the machine (unless it has been installed). A large part of interacting with these systems is using the terminal.

The terminal is purely text-based and it is intimidating at first. However, if we break down some of the commands, after some time, you quickly become familiar with using the terminal.

``tryhackme@linux1:~$ enter commands here``

We need to be able to to do basic function like navigate to files, output their contents and make files. The commands to perform these actions are self-explanatory. Let's get started with two of the first commands which are broken down in the table below:

Basic commands:


``echo`` - output any text that we provide

``whoami`` - find out which user we're currently logged in as 


See the snippets below for an example of each command being used:

<img src="images/linux-command1.png" width="500" />


Note: When using the ``echo`` command in Linux, single words do not require double quotes (e.g., ``echo Hello``). However, strings containing spaces must be enclosed in double quotes (e.g., ``echo "Hello Friend!"``).

`whoami` can be used to find the username we're logged in as.

<img src="images/linux-command2.png" width="500" />

# Task 5 Interacting With the FileSystem!

## Navigating and Exploring Files in Linux

As mentioned earlier, navigating a Linux machine without relying on a desktop environment is crucial. The terminal is your main tool for moving around and managing files and directories.

### Key Commands

| Command | Full Name           | Description                                                                 |
|---------|---------------------|-----------------------------------------------------------------------------|
| ls      | listing             | Lists files and directories in the current directory                        |
| cd      | change directory    | Changes the current working directory                                       |
| cat     | concatenate         | Outputs the contents of a file                                              |
| pwd     | print working directory | Shows the full path of the current working directory                    |

---

### Listing Files (`ls`)

Before doing anything with files or folders, you need to know what exists in the current directory. Use the `ls` command to list the contents. 

You can also list the contents of a specific directory without navigating to it: `ls Pictures`


### Changing Directories (`cd`)

To move into a directory, use the `cd` command followed by the directory name: ``cd Pictures``


Then you can, use `ls` again to see the contents of the new directory.


### Viewing File Contents (`cat`)

To view the contents of a file, use the `cat` command.  `cat todo.txt`

This will output the contents of `todo.txt`. You can also use `cat` with the full file path:

`cat /home/ubuntu/Documents/todo.txt`


This is especially useful for quickly checking configuration files, notes, or other text files.


### Finding Your Current Location (`pwd`)

If you ever get lost, use the `pwd` command to print the full path of your current working directory:

`/home/ubuntu/Documents`


This helps you keep track of where you are in the filesystem.

## Summary

- **`ls`** – List files and directories
- **`cd`** – Change directory
- **`cat`** – View file contents
- **`pwd`** – Show current directory path

Mastering these commands is essential for efficient navigation and management of files in Linux.









