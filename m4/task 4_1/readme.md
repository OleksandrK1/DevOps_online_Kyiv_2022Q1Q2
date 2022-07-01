### EPAM University Programs DevOps external course
## Module – Linux Networking
# Task 4.1
Task1.Part1 

__Please note!!!__ All Answer in ___BOLD Itallic!___
1) Log in to the system as root (or sudo-er).

    ___sudo -s___ or ___sudo -i___
2) Use the passwd command to change the password. Examine the basic parameters of the command. What system file does it change *?

    ___passwd___
    ____/etc/shadow____
3) Determine the users registered in the system, as well as what commands they execute. What additional information can be gleaned from the command execution?

    ___w___
    ___id___
    ___last___
4) Change personal information about yourself.
Answers:
    ___usermod___
5) Become familiar with the Linux help system and the man and info commands. Get help on the previously discussed commands, define and describe any two keys for these commands. Give examples.

    ___man -f passwd___ - displays short info
    ___man -k usermod___ - looking for keyword, in our case it is usermod
6) Explore the more and less commands using the help system. View the contents of files .bash* using commands.

    ___man more___
    ___man less___
7) * Determine the last logon time for all users. Tip: You should read the documentation for the finger command.
8) * List the contents of the home directory using the ls command, define its files and directories. Hint: Use the help system to familiarize yourself with the ls command.

Task1.Part2 

1) Examine the tree command. Master the technique of applying a template, for example, display all files that contain a character c, or files that contain a specific sequence of characters. List subdirectories of the root directory up to and including the second nesting level.
    ___sudo tree -f -P c*___ 
    or 
    ___sudo tree -f -P somename*___ 
    
    ___sudo tree -ad -L 2___
    
2) What command can be used to determine the type of file (for example, text or binary)? Give an example.
    ___file filename.txt___
    
3) Master the skills of navigating the file system using relative and absolute paths. How can you go back to your home directory from anywhere in the filesystem?

    ___cd ~___

4) Become familiar with the various options for the ls command. Give examples of listing directories using different keys. Explain the information displayed on the terminal using the -l and -a switches.
___ls -d */___
___ls -l___ - command to list the contents of the directory in a table format with columns including: content permissions,  number of links to the content, owner of the content, group owner of the content, size of the content in bytes, last modified date / time of the content, file or directory name
___ls -a___ - command to list all files (including hidden) or directories 

5) Perform the following sequence of operations:
- create a subdirectory in the home directory;
    ___sudo mkdir /home/subdir/___
- in this subdirectory create a file containing information about directories located in the root directory (using I/O redirection operations);
    ___cd /home/subdir/___
    ___sudo -s___
    ___ls / > file.txt___
- view the created file;
    ___cat file.txt___
- copy the created file to your home directory using relative and absolute addressing.
___cp file.txt ~/___
___cp file.txt /home/alex/___
- delete the previously created subdirectory with the file requesting removal;
___sudo rm -r /home/subdir/___
- delete the file copied to the home directory.
___rm ~/file.txt___
6) Perform the following sequence of operations:
- create a subdirectory test in the home directory;
___mkdir ~/test___
- copy the .bash_history file to this directory while changing its name to labwork2;
___cp .bash_history ~/test/labwork2___
- create a hard and soft link to the labwork2 file in the test subdirectory;
___ln -s labwork2 labwork2.link___
- how to define soft and hard link, what do these concepts;
___hard link has content of original file, soft links has only the path of the original file, not the contents___
- change the data by opening a symbolic link. What changes will happen and why
___echo "added text" >> labwork2.link___
___original file has changed___

- rename the hard link file to hard_lnk_labwork2;
___mv labwork2 hard_lnk_labwork2___
- rename the soft link file to symb_lnk_labwork2 file;
___mv labwork2.link symb_lnk_labwork2___
- then delete the labwork2. What changes have occurred and why?
___No such file___ ___we renamed it two steps before___ 
7) Using the locate utility, find all files that contain the squid and traceroute sequence.
___locate -A squid*___
___locate -A traceroute*___
8) Determine which partitions are mounted in the system, as well as the types of these partitions.
___lsblk___
9) Count the number of lines containing a given sequence of characters in a given file.
___wc -l givenfile___
10) Using the find command, find all files in the /etc directory containing the host character sequence.
___find ./etc -type f -name "host*"___
11) List all objects in /etc that contain the ss character sequence. How can I duplicate a similar command using a bunch of grep?
___find ./etc -name "ss*"___
12) Organize a screen-by-screen print of the contents of the /etc directory. Hint: You must use stream redirection operations.
___ls -la | more___
13) What are the types of devices and how to determine the type of device? Give examples.
14) How to determine the type of file in the system, what types of files are there?
___file somenameof.file___
___regular files, directories, special files like links or hidden_____
15) * List the first 5 directory files that were recently accessed in the /etc directory.
___ls -dt | head -n 5___

