# Final Notes 

## Notes 1
### What is Ubuntu?

### What is Ubuntu?
Ubuntu is a complete Linux operating system, freely available with both community and professional support. Ubuntu is
suitable for both desktop and server use. The current Ubuntu release supports Intel x86 (IBM-compatible PC), AMD64
(x86-64), ARMv7, ARMv8 (ARM64), IBM POWER8/POWER9 (ppc64el), IBM Z zEC12/zEC13/z14 and IBM LinuxONE
Rockhopper I+II/Emporer I+II (s390x). Ubuntu includes thousands of pieces of software, starting with the Linux kernel
version 5.4 and GNOME 3.28, and covering every standard desktop application from word processing and spreadsheet
applications to internet access applications, web server software, email software, programming languages and tools and
of course several games.

### A little bit of Ubuntu's background
### The Ubuntu Vision
* In April 2004 Mark Shuttleworth brought together a group of developers from the Debian project, GNOME, and
GNU. The goal of the meeting was to answer the following questions:
* Is a batter type of operating system possible?
* What would this OS look like?
* Can you describe the community that would build this project?

 The team called itself The Warthogs and set on to build the Ubuntu operating system
 * Before Ubuntu, installing Linux was a project for computer enthusiasts. Linux on the desktop was considered a
computer nerd only operating system because it was difficult to install and maintain for a regular computer user.
* Ubuntu 4.10 (Warty Warthog), released on 20 October 2004. It was Canonical's first release of Ubuntu and it
looked like this: 
![UbuntuDesktop](Capture.PNG)
* Ubuntu 6.06 (Dapper Drake), released on 1 June 2006, was Canonical's fourth release and the first long-term
support (LTS) release. It looked like this:
![UbuntuDesktop2](Capture2.PNG)

### Ubuntu Flavors 
An ubuntu flavor is an operating system based on ubuntu that uses a different desktop environment than the default
Ubuntu’s desktop environment (GNOME). Ubuntu flavors offer a unique way to experience Ubuntu, each with their own
choice of default applications and settings. Ubuntu flavors are backed by the full Ubuntu archive for packages and
updates.

### UBuntu has 7 official flavors
Logo|Flavor|Download List
-----|-----|-----
![KubuntuLogo](Kubuntu.PNG)|Kubuntu|https://kubutntu.org/getkubuntu/
![LubuntuLogo](Lubuntu2.PNG)|Lubntu|https://lubuntu.net/downloads/
![UbuntuBudgie](Budgie.PNG)|Ubuntu Budgie|https://ubuntubudgie.org/downloads
![UbuntuKylin](Kylin.PNG)|Ubuntu Kylin|https://ubuntukylin.com/downloads/show.php?id+451&lang=en
![UbuntuMate](Mate.PNG)|Ubuntu Mate|https://ubuntu-mate.org/download/
![UbuntuStudio](Studio.PNG)|Ubuntu Studio|https://ubuntustudio.org/download/
![Xubuntu](Xubuntu.PNG)|Xubuntu|https://xubuntu.org?download/

Ubuntu also serves as a base for a large number of Linux distributions. Some people call those Linux distributions Ubuntu
distributions because they heavily rely on Ubuntu’s active development cycle

### Some UBuntu distributions are: 
* Linux Mint
* Pop!_OS
* elementary OS
* Zorin OS
* Linux Lite
* Peppermint OS
* BackBox Linux

## Notes 2

### What is Virtualization?
* Replication of Hardware used to simulate a virtual machine inside a physical machine 
### Using Virtual Box 
* Open source software 
* Runs on windows, Linux, Mac, and Solaris 
* needs a computer with powerful enough components
* * needs at least 
  * amd v or intel v 
  * dual core x64b processor wit h1.3 
  * 4bg of ram
  ### Installing Ubuntu in a Virtual Machine 
  #### settings for the virtual environment 
* 2 GB of Ram
* 50 GB of storage ( if available)
* at least a dual core processor ( 1 core can work but not as well)
* video 64MB  or Higher
* Audio - disabled 
* Shared clip board and Drag and Drop - Bidirectional 
* Must download Ubuntu Rom (Ubuntu 20.04 64 bit) and select it under storage in VM settings 
### what is Raspberry Pi?
* Low cost credit card sized computer that plugs into a monitor or tv and uses a standard keyboard and mouse 

## Notes 3

### Exploring Desktop Environment
* a collection of software that allows you to use the computer 
* before a Desktop Environment (DE) there was a Command Line (CLI)
* Plethora of graphical desktops avail
  * for ex
  GNOME| KDE| XFCE|
  |MATE| BUDGIE| LXDE|
  |Cinnamon| Openbox| LXQT|
  |Pantheon| Deeping DE| Fluxbox|

* Graphical User Interface (GUI)- a set of programs that allows user to interact with computer system via icon windows and various DE implementations
  ex. implementations 
* Display Manager (linux)
* File Manager (Windows)
* Icons- representation of programs
* Panel- Slim rectangular area at the very top or bottom of desktops, contain notifications 
### What is a Shell?
* GNU bash shell is a program that provides interactive access to the Linux System
* runs a regular program and is normally started whenever a user logs into a terminal
* Most Linux distros use the bash shell as default but there are others like:
  * Tcsh shell
  * Csh shell
  * Ksh shell
  * Zsh shell
  * Fish shell
### Managing software 
* Package- archives that contain binaries of software, configuration files, and information about dependencies. (in windows, commonly known as .exe files.' compressed' )
* Library- reusable code that can be used by more than one function or program
* Dependency- software need as a foundation for other software
* Repository- a large collection of software available for download
  * Ubuntu repositories 
    * Main- canonical- supported fee and open source software
    * universe- community-maintained free and open source software 
    * Restricted- Proprietary drivers for devices
    * Multiverse- software restricted by copyright or legal issues
### Debian Package Management System 
* DPMS is the foundation for managin softwarte on all debian distributions
* at the core if DPMS is the dpkg
* debian package names end with the .deb extension are called ".deb files"  
* dpkg is a low level tool. therefore wrapper tools are preferred since dpkg cannot handle dependencies 
  
 ### Linux Filesystem 
* File System: The way files are stored and organized to simplify access to data.
* organizes files in what is called *hierarchal directory structure (tree-like pattern of folders) 
* Directory and folder mean the same thing 
* first directory is called the *root* directory. The root contains files and sub directions 
* File System Hierarchy Standard (FHS)- specifies requirements and guidelines for file and directory placement in UNIX like operating systems
 * Linux always have a single file system tree, regardless of how many drives or storage devices are attached to the computer.

## Notes 4

### Linux Directory System
### File system
* way fiels are stored and organized
* linux and mac use **hierarchial directory structure ( tree like pattern of folders) 
* Directory = Folder 
* File System Hierarchy Standard (FHS) specifice requirements and guidelines for files and diectroy placement in UNIX like OSs
* Root Directory is the god file contains files and sub directories 
* Unlink windows  linux always have a single file system tree regardless of how many drives or storage devices are attached to the computer 
* In linux everything is a file 
### The Nemo File Manager
* include picture
Think of the file system as a tree, every branch and branches of those branches are files 
your are always working in a file 
Parent Directory
    Child directory 
    Pathname directory ex: /home/otm/license
* always want to start at your home directory to prevent issues 
  
  include directory pic 

### Commands to move around the file system 
* The pwd command- used for displaying the current working directory 
* The cd command- used for changing directory 
  cd../ = backwards, parent directory 
  cd . = current directory 
  cd = will take you home 

* The ls command- used for displaying all the files inside a given directory.
  
### types of path names 
* absolute path states the full pathname starting from root. Always starts from root. works from anywhere 
  
* relative path works with files relative to current file location. specifies the pathname starting from the current directory. always starts with a subdirectory 

### Listing Files And Directories 
* ls is used for listing content of given directory 
  ls --help lists all ls commands 
  master pwd cd an ls commands 

## Notes 5
======
# Handling Text Files 
* CAT command used for displaying contents of file
  * concatenate - to join two strings together, two files together, two texts together
  * CAT + (a single file) =  list content of the single file 
  * cat -n to view line numbers 
  * cat -b to display content of file with line numbers excluding empty lines.
  * cat -E displays $ at end of every line so you know where the end of the line is
  *  
* CAT command can also serve as a text editor 
* TAC command 
* works like cat but displays list from bottom to top 

* More command
  * a pager program used for displaying the context of text files one page at a time
  * more -d open a file and display guding info in the bottom 
  * more -10 open a file 10 lines at a time 

* Less command - faster than more 
* les -N to file a line 

* Head command - displays the top N number of lines 
* -1 displays the first line of the file

* Cut command - extracts specific sections of lines of a file and display it to the screen
* cut -b 
* the limiter is any character that allows you to divide file into columns
* ex cut + option + file 
* cut -f1 displays the fist field of each line, using : as the field separator 
* etc/passwd contains 
* cut -d : -f1 /etc/passwd displays the first field of each line, using: as the field separator 
* ex cut -d '-' f1 
*

* Sort commmand 

wc command - used for printing the number of lines characters and bytes in a file 
wc -c disp number of bytes 
wc -l disp number of lines 
wc -m dsip number of characters in a file 
wc -w disp number of words in a file 

* tr command - used for translation or deleting characters from standard output

* diff command compares files and display the difference 
  * diff file1 file2

* display the diff btw two files 

## Grep command 
used to match a string pattern from a file or a standard output when using the pipe
* Usage: grep + option + pattern to match file
* standard output+pipe (|) + grep + pattern to match 
* grep - 'grab'
* grep -i turns case sens. off
* grep -n Displays line number of each line matched
* grep -E treats the pattern as an extended_regular_expression grep -V Inverts the search
* grep -o only display the string matched 

^ in the beginning is a reg expression that tells grep to give lines that start with specified word
$ is the same but finds the specfied word at the end 

## I/O redirection 
* can redirect the input and output of command to and from files as well as connect multiple commands together into powerful command pipelines
* The commands learned so far generatie 2 types of output
  * The result of the command 
  * Error when the command does not run
  * since every thing in linuc is a file, thes programs send rher output to a file called STDOUT and error messages to STDERR
  * These files arelinked to the sceen by defualt which means that they are not saved into a file but instead disaplayed in the terminal 
  * Input is sent ti STDIN and is attacheh to the keyboard in the same way that STDOUT and STDERR are attached to the display by default 
  * I/O redirection allows us to change where output goes and where input comes from
  
  Standard File Descriptors
  File Descriptor|
  ---------------|-----------|--------|
  0 STDOUT
  1 STDIN
  3 STDERR

  ex. 
  ls Downloads/> filesIhave.txt overwrites

  ls Downloads/>> filesIhave.txt appends or attaches

(|) The pipe allows you to redirect the standard output 

Alias - a shorthand for a more complicated command
* alias name_of_alias= "command here"
