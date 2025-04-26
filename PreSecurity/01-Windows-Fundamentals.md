# Task 1 Introduction to Windows

This is a basic introduction to the Windows OS. The main objective is to start the Virtual Machine.
We have two options:
- Start Machine in the web browser.
- Open Virtual Machine via Remote Desktop and log in with the provided credentials.

I picked the first option and logged in through the web browser.

# Task 2 Windows Editions

## What is an OS?

An Operating System is the main software that manages all hardware and software on a computer. It acts as a bridge between the machine and the user, allowing programs to run and devices to communicate.

Windows has a long history, dating back to 1985, and is still the dominant operating system in both home and corporate networks. Due to its popularity, Windows OS has always been a target for threat actors.

The authors in this section take us through the history of Windows, up to the latest version, Windows 11.

Windows 10 comes in two versions: Home and Pro. These two versions are different from each other.

The current Windows operating system for servers is Windows Server 2019, and for the attached virtual machine, we also use Windows Server 2019 Standard.

Objective of this task is to answer the question:

**What encryption can you enable on Pro that you can't enable in Home?**

The correct answer is BitLocker.

## What is BitLocker?

BitLocker protects your computer from unauthorized access by encrypting the entire drive. It's the default Windows encryption system and encrypts the C: drive to keep your data safe.

# Task 3 The Desktop (GUI)

## What is GUI?

A Graphical User Interface (GUI) lets users interact with devices through icons and visual elements, instead of typing commands. GUIs were developed to be more user-friendly than Command-Line Interfaces. (CLIs)


<img src="images/screen.png" width="800" />
<small>Image Source: Wikipedia</small>


## What is CLI?

A Command-Line Interface is a way of interacting with a computer by typing text commands into a terminal or console.

<img src="images/screen1.png" width="800" />
<small>Image Source: Wikipedia</small>

--- 

In short:
- GUI = Click buttons
- CLI = Type commands

CLIs are powerful and efficient for advanced users, but they are hard to learn for beginners. This was the reason why GUIs were created!


In this section, the authors provide basic information about the Windows GUI, but I decided not to include that in my notes since I've been a Windows user since I was a kid, I didn't feel the need to include it in my notes.

---

Objective of this task is to answer 3 questions:

**Which selection will hide/disable the Search box?**

Answer: Hidden

**Which selection will hide/disable the Task View button?**

Answer: Show Task View button

**Besides Clock and Network, what other icon is visible in the Notification Area?**

Answer: Action Center


# Task 4 The File System

## What is a File System?

A file system organizes and stores data on a storage device. Without a file system, data would be scattered randomly, and the computer wouldn’t know how to access it. It ensures data is ordered and accessible.

## What is FAT?

The File Allocation Table (FAT) is a simple file system that uses a table at the top of the volume to keep track of file locations.

## FAT characteristics:

- Two copies of FAT for protection.
- Used in USB drives, SD cards, external drives, and consoles etc.

## Limitations:

- Maximum size: 2TB partition, 4GB file.
- Poor performance with large volumes.
- No file permissions.
- Inefficient space use.

## What is exFAT?

exFAT is an improved version of FAT32 with no practical size limits on files or partitions.

## Limitations:

- Less compatibility than FAT32 (some older devices and Linux versions may not support it).

## What is NTFS?

NTFS (New Technology File System) is the primary file system for modern Windows systems. It is a journaling file system, meaning it can repair itself using log files after a failure.

## NTFS improvements:

- Limitless file/partition size.
- File/folder permissions.
- File compression.
- Encryption (Encryption File System or EFS).

You can check your system’s file system by looking at the Properties of your hard drive.

## File and Folder Permissions

Permissions allow you to grant or deny access to files and folders. The image below shows how these permissions work:

<img src="images/screen2.png" width="800" />
<small>Image Source: Microsoft</small>

## Alternate Data Streams (ADS)

ADS is a function of NFTS, which allows to hide data in "second stream" ("") of the file. Every file has at least one data stream and ADS allows files to contain more than one stream of data.

For example Windows Explorer doesn't display ADS to the users. There are 3rd party exectuables that can be used to see the data or you can use Powershell that gives you ability to view ADS for files ($DATA)

$DATA is a type of data stream.

These data streams have bad reputation since they have been used and abused by malware writers to write hidden data varying from data about where a file came from to complete malware files.

## In short:

ADS is a feature of NTFS that allows files to have more than one data stream. While Windows Explorer doesn’t show ADS, tools like PowerShell can display it.


# Task 5 The Windows\System32 Folders 

`C:\Windows` is known as the main folder which contains the Windows opearting system.
It doesn't mean that it always need to be in drive C necessairly. It can reside in any other drive and folder.

In windows, 
%windir%
 is an environment variable in Windows that points to the folder where the Windows OS is installed. 

 ## Windows32

The System32 folder holds the most important files that are critical for the operatin system! 

Many of the files in System32 are required to run Windows. If this folder id deleted or damaged it can cause the entire system to crash or become unstable, you should proceed with extreme caution when interacting with this folder.

Objective for this task was to answer the question:

**What is the system variable for the Windows folder?**

%windir%












