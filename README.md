                                                                   Linux 🐧

What is Linux?

Linux is a free, open source operating system that enables the communication between computer hardware and software. The Linux OS was developed by Linus Torvalds in 1991.

Why use Linux?

Open source

Community Support

Support wide variety of hardware

Most servers runs on Linux

Secure compared to Windows

Linux distributions

There are many Linux distributions available in the market. It provides a different flavor of the Linux operating system to the users. Popular distros are :

Ubuntu

Fedora

Debian

Linux Mint  and so on.

Linux File System

Linux provides a dedicated set of file systems that stores every bit of data required for booting up the Linux systems. The file system holds the collection of data or files stored within the computer's hard disk or storage device.

Use "man heir" to find more insights on linux files system


ls /etc/ 

This directory contains all the configuration files of your application. if something goes wrong you should be looking in this directory.


ls /bin

This directory contains binaries for use by all users and also contains executable files, Linux commands that are used in single user mode, and common commands that are used by all the users, like cat, cp, cd, ls, etc

ls /sbin

This directory contains binaries to configure the operating system and executable files. It only contains system binaries which require root privilege to perform certain tasks and are helpful for system maintenance purposes. e.g. fsck, root, init, ifconfig, etc

ls /lib

This directory contains shared libraries which are often used by the ‘/bin’ and ‘/sbin’ directories. It also contains a kernel module. These filenames are identable as ld* or lib*.so.*

ls /opt

This directory's main purpose is to store optional application software packages. In many cases this is software from outside the distribution repository. Add-on applications from individual vendors should be installed in ‘/opt’. In some systems ‘/opt’ is empty as they may not have any add-on application.

ls /tmp

This directory in Linux based systems contains necessary files that are temporarily required by the system as well as other software and applications running on the machine.

For example, when you are writing a document, all the content inside that document is saved as a temporary file inside the /tmp directory. After you have saved it, it gets stored in your preferred location, and the temporary file gets removed once you exit the document.

ls /boot

This directory contains the linux boot configuration files. This is one of the MOST important folders. Removing anything from this directory or a file getting corrupted will result in an OS crash after reboot. Your system won't be able to boot without files in the /boot directory.


ls /dev

This directory contains files that represent devices that are attached to the local system. However, these are not regular files that a user can read and write to; these files are called device files or special files. Device files are abstractions of standard devices that applications interact with via I/O system calls.

ls /media

The /media directory contains subdirectories where removable media devices inserted into the computer are mounted. For example, when you insert a CD into your Linux system, a directory will automatically be created inside the /media directory. You can access the contents of the CD inside this directory.

ls /mnt

This directory and its subdirectories are intended for use as the temporary mount points for mounting storage devices, such as CDROMs, floppy disks and USB (universal serial bus) key drives. /mnt is a standard subdirectory of the root directory on Linux


ls /proc
This directory is for each process running on our system. It also contains some configuration files
ls /var
This directory contains variable data files. This includes spool directories and files, administrative and logging data, and transient and temporary files.
There are 7 types of files in Linux
Normal files
Directories
References to files
Character device files
Block device files
Symbolic links
Local domain sockets/named pipes


Find more info about files in the directory 
ls -l
Sort files based on timestamp
ls -lt
Sort files based on timestamp in descending order
ls -ltr
Monitoring in Linux
Configured in /etc/monitrc
Install Monit
apt-get update
apt-get install monit
systemctl enable monit
systemctl start monit
Edit /etc/monit/monitrc
    systemd
systemd is monitoring init system used to manage services
systemctl <command> <unitname>
Log management commands
Journalctl
journactl -u
journactl --since "2 min ago"






Linux Directory Commands
1. pwd Command
The pwd command is used to display the location of the current working directory.
Syntax: pwd  
2. mkdir Command
The mkdir command is used to create a new directory under any directory.
Syntax: mkdir <directory name>  
3. rmdir Command
The rmdir command is used to delete a directory.
Syntax: rmdir <directory name>  
4. ls Command
The ls command is used to display a list of content of a directory.
Syntax: ls  
Linux File commands
6. touch Command
The touch command is used to create empty files. We can create multiple empty files by executing it once.
Syntax: touch <file name>  
               touch <file1>  <file2> ....  




7. cat Command
The cat command is a multi-purpose utility in the Linux system. It can be used to create a file, display content of the file, copy the content of one file to another file.
Syntax: cat [OPTION]... [FILE]..  
To create a file, execute it as follows:
cat > <file name>  
// Enter file content  Press "CTRL+ D" keys to save the file. 
To display the content of the file, execute it as follows:
cat <file name>  
8. rm Command
The rm command is used to remove a file.
Syntax: rm <file name>
9. cp Command
The cp command is used to copy a file or directory.
Syntax: cp <existing file name> <new file name>  
11. rename Command
The rename command is used to rename files. It is useful for renaming a large group of files.
Syntax: rename 's/old-name/new-name/' files  
For example, to convert all the text files into pdf files, execute the below command: rename 's/\.txt$/\.pdf/' *.txt 
Linux File Content Commands
12. head Command
The head command is used to display the content of a file. It displays the first 10 lines of a file.
Syntax: head <file name>  
13. tail Command
The tail command is similar to the head command. The difference between both commands is that it displays the last ten lines of the file content. It is useful for reading the error message.
Syntax: tail <file name>  
14. tac Command
The tac command is the reverse of cat command, as its name specified. It displays the file content in reverse order (from the last line).
Syntax: tac <file name>  
15. more command
The more command is quite similar to the cat command, as it is used to display the file content in the same way that the cat command does. The only difference between both commands is that, in case of larger files, the more command displays screenful output at a time.
In more command, the following keys are used to scroll the page:
ENTER key: To scroll down page by line.
Space bar: To move to the next page.
b key: To move to the previous page.
Syntax: more <file name>  
16. less Command
The less command is similar to the more command. It also includes some extra features such as 'adjustment in width and height of the terminal.' 
Syntax: less <file name>  
Linux User Commands
17. su Command
The su command provides administrative access to another user. In other words, it allows access of the Linux shell to another user.
Syntax: su <user name> 
18. id Command
The id command is used to display the user ID (UID) and group ID (GID).
Syntax: id  
19. useradd Command
The useradd command is used to add or remove a user on a Linux server.
Syntax: useradd  username 


20. passwd Command
The passwd command is used to create and change the password for a user
Syntax: passwd <username>  
21. groupadd Command
The groupadd command is used to create a user group.
Syntax: groupadd <group name>  
Linux Filter Commands
22. grep Command
The grep is the most powerful and used filter in a Linux system. The 'grep' stands for "global regular expression print." It is useful for searching the content from a file. Generally, it is used with the pipe.
Syntax: command | grep <searchWord>  
23. comm Command
The 'comm' command is used to compare two files or streams. By default, it displays three columns, first displays non-matching items of the first file, second indicates the non-matching item of the second file, and the third column displays the matching items of both files.
Syntax: comm <file1> <file2>  
24. sed command
The sed command is also known as stream editor. 
Syntax:  command | sed 's/<oldWord>/<newWord>/'  


25. tee command
The tee command is quite similar to the cat command. The only difference between both filters is that it puts standard input on standard output and also write them into a file.
Syntax: cat <fileName> | tee <newFile> |  cat or tac |.....  
26. gzip Command
The gzip command is used to truncate the file size. It is a compressing tool. It replaces the original file by the compressed file having '.gz' extension.
Syntax: gzip <file1> <file2> <file3>... 
27. gunzip Command
The gunzip command is used to decompress a file. It is a reverse operation of gzip command.
Syntax: gunzip <file1> <file2> <file3>. .  
28. sleep Command
The sleep command is used to hold the terminal by the specified amount of time. By default, it takes time in seconds.
Syntax: sleep <time>  
29. zcat Command
The zcat command is used to display the compressed files.
Syntax: zcat <file name>  


30.df Command
The df command is used to display the disk space used in the file system. It displays the output as in the number of used blocks, available blocks, and the mounted directory.
Syntax: df  
31. clear Command
Linux clear command is used to clear the terminal screen.
Syntax: clear  
32. ip Command
Linux ip command is an updated version of the ipconfig command. It is used to assign an IP address, initialize an interface, disable an interface.
Syntax: ip a or ip addr 
33. ssh Command
Linux ssh command is used to create a remote connection through the ssh protocol.
Syntax: ssh user_name@host(IP/Domain_name)</p>  
34. mail Command
The mail command is used to send emails from the command line.
Syntax: mail -s "Subject" <recipient address>  






35. ping Command
The ping command is used to check the connectivity between two nodes, that is whether the server is connected. It is a short form of "Packet Internet Groper."
Syntax: ping <destination>  
36. host Command
The host command is used to display the IP address for a given domain name and vice versa. It performs the DNS lookups for the DNS Query.
Syntax: host <domain name> or <ip address>  






















Installing a Linux Virtual Machine					
There are a variety of ways to install a Linux System.
For example,if you are currently running Windows as your primary operating system, then you may be able to dual boot Linux alongside Windows, but this method is not beginner-friendly. 
What is a Virtual Machine?					
A virtual machine is simply a computer running from within another computer (host). A virtual machine shares the host resources and behaves exactly like a standalone physical machine. 					
The process of installing a virtual machine is straightforward; you only need to follow the following steps:	
1.InstallVirtualBox(orVMwarePlayer).					
2. Download an ISO image of any Linux distribution.
3. Open up VirtualBox and begin the installation process. 
Download VirtualBox at the following link: www.virtualbox.org/wiki/Downloads 		
Download Ubuntu LTS at the following link: www.ubuntu.com/download/desktop 




















Setup for Ubuntu
First, open VirtualBox, then click "New" to create a virtual machine.



NOTE: Select any amount of memory you wish, but don't add more than 50 percent of your total RAM.
Check the "Create a virtual hard disk now" option so we can later define our Ubuntu OS virtual hard disk size. Now, we want to select "VHD (Virtual Hard Disk)".




Next, we'll dynamically allocate storage on our physical hard disk



We want to specify our Ubuntu OS's size. The recommended size is 10 GB, but you can increase the size if you wish.






After creating a virtual hard disk, you'll see Ubuntu in your dashboard.

Now, we have to set up the Ubuntu disk image file (.iso).The Ubuntu disk image file can be downloaded here: Ubuntu OS download

To set up the Ubuntu disk image file, go to settings and follow these steps:
Click "Storage"
In storage devices, click "Empty"
In attributes, click the disk image and "Choose Virtual Optical Disk File"
Select the Ubuntu disk image file and open it

Click OK.
Your Ubuntu OS is ready to install in VirtualBox. Let's start!

NOTE: Ubuntu VirtualBox installation and actual OS installation steps may vary. This guide helps you to install Ubuntu in VirtualBox only.
Let's install Ubuntu!
Click Install Ubuntu.

Select your keyboard layout.

In the "Updates and other software" section, check "Normal installation" and continue.

In "Installation type", check "Erase disk and install Ubuntu".

Click "Continue".

Choose your current location.

Now, set up your profile.

You'll see Ubuntu installed.

After the installation, restart it.

After logging in, you'll see the Ubuntu desktop.











Successfully installed Ubuntu in VirtualBox. It's ready to use for your future development projects.
Verify the installation.Open your terminal (Press Ctrl+Alt+T) and type in the commands below and check if they work-  pwd: This will print the current working directory, 				
			
		


				
			
		

