# Exploring Desktop Environment
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
# What is a Shell?
* GNU bash shell is a program that provides interactive access to the Linux System
* runs a regular program and is normally started whenever a user logs into a terminal
* Most Linux distros use the bash shell as default but there are others like:
  * Tcsh shell
  * Csh shell
  * Ksh shell
  * Zsh shell
  * Fish shell
# Managing software 
* Package- archives that contain binaries of software, configuration files, and information about dependencies. (in windows, commonly known as .exe files.' compressed' )
* Library- reusable code that can be used by more than one function or program
* Dependency- software need as a foundation for other software
* Repository- a large collection of software available for download
  * Ubuntu repositories 
    * Main- canonical- supported fee and open source software
    * universe- community-maintained free and open source software 
    * Restricted- Proprietary drivers for devices
    * Multiverse- software restricted by copyright or legal issues
  ## Debian Package Management System 
  * DPMS is the foundation for managin softwarte on all debian distributions
  * at the core if DPMS is the dpkg
  * debian package names end with the .deb extension are called ".deb files" 
  * dpkg is a low level tool. therefore wrapper tools are preferred since dpkg cannot handle dependencies 
  
  # Linux Filesystem 
  * File System: The way files are stored and organized to simplify access to data.
  * organizes files in what is called *hierarchal directory structure (tree-like pattern of folders) 
  * Directory and folder mean the same thing 
  * first directory is called the *root* directory. The root contains files and sub directions 
  * File System Hierarchy Standard (FHS)- specifies requirements and guidelines for file and directory placement in UNIX like operating systems
  * Linux always have a single file system tree, regardless of how many drives or storage devices are attached to the computer.
