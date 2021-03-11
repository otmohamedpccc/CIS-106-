Notes-4
# Linux Directory System
# File system
* way fiels are stored and organized
* linux and mac use **hierarchial directory structure ( tree like pattern of folders) 
* Directory = Folder 
* File System Hierarchy Standard (FHS) specifice requirements and guidelines for files and diectroy placement in UNIX like OSs
* Root Directory is the god file contains files and sub directories 
* Unlink windows  linux always have a single file system tree regardless of how many drives or storage devices are attached to the computer 
* In linux everything is a file 
# The Nemo File Manager
* include picture
Think of the file system as a tree, every branch and branches of those branches are files 
your are always working in a file 
Parent Directory
    Child directory 
    Pathname directory ex: /home/otm/license
* always want to start at your home directory to prevent issues 
  
  include directory pic 

# Commands to move around the file system 
* The pwd command- used for displaying thre current working directory 
* The cd command- used for changing directory 
  cd../ = backwards, parent directory 
  cd . = current directory 
  cd = will take you home 

* The ls command- used for displaying all the files inside a given directory.
  
## types of path names 
* absolute path states the full pathname starting from root. Always starts from root. works from anywhere 
  
* relative path works with files relative to current file location. specifies the pathname starting from the current directory. always starts with a subdirectory 

# Listing Files And Directories 
* ls is used for listing content of given directory 
  ls --help lists all ls commands 
  master pwd cd an ls commands 
# Managing Files amd Directories 
* Getting help
  * Man (Manual) Pages 