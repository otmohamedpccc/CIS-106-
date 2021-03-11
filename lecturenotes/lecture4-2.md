
# options and arguments 
* commands are often followed by options that modify/enhance their behavior 
# Creating files and directories 
## creating directories 
* the mkdir is used for creating a single directory or multiple directories 
* to create a directory with mkdir type: mkdir + the name of directory 
* to create multiple directories separate names it a space 
* string is a value of data 
* you can create  a directory with a space in its name use the escape character \ ex elder\scrolls 
* mkdir 'elder scrolls' makes a new folder names elder scrolls 
* when in root to make a folder you must use absolute path. need to use full path name 

# creating files
* the touch command 
* intended for modifying time stamps 
* to create a touch list 
  * touch list 
* # Deleting files and directories 
* rm command 
* cannot remove non empty directories, must be empty before removing.
* rmdir - is the command 
* rm -r : the -r is recursive 
  # moving files and directories
  * the mv command 
  * can remove or rename things 
  * basic formula
    * mv + source + destination 
    * to rename mv + file/directory to rename + new name 
    * both source and destination can be absolute path or relative path
    * ~ means home and user directory 
    * moving one folder to another 
      * mv ~/downloads/laptops ~pictures/laptops2.0
# copying files and directories 
* the cp command
  * cp copies files/ directories (need to use -r with directories) 
  * include pic from slide 
  ![cpcommands](cpcommands.png) 

# Common mistakes people make using mv
link 

# working with links (think oh shortcuts)
* what is an inode?
* a data structure that contains all the info about a file 
* every file in a system has an inode
* each inode is identified by an inode number index (index number)

# Hardlinks 
  * files that points to data on the hard drive 
  * when you create a file its automatically linked to the data 
  * Hard links must be created on the same partition 
  * basic command 
    * ln shoppinglist.txt

# Soft links
* special type of file that pint to other files instead of datanin the hard drive 
* soft links do not share the same inode number as hard links do 
* if you modify a soft link the target file is modified aswell
* to create symbolic link ln -s file fileSL

# getting help from your computer 
* man (manual) pages are documentation files that describe the linux shell
* man pages are not step by step guides, but instead quick references 
* To view the manual of a command type: man+command
  * Example: man ls
  * To navigate the man page of command, you can use the arrow key or the man command internal shortcuts
  * to exit the man pages press the letter q 
# other ways of getting help
* -h --h --help
* info, ex info exa 
* apropos goes through each man page and searches given command 
* read error messages carefully. Most of the time the answer is in te error itself 
* whatis to install cheat use the command sudo snap install cheat
* some commands many not have a man page but an info page. To read the info page of a command use 

# using wild cards/ File Globbing
* Wildcards represents letters and characters used to specify a filename for searches
* File Globbong is the processing of pattern matching using wildcards
* wild cars aka metacharacter wildcards
# 3 Types of wild cards 
the * - matches everything or nothing 
main wild card is * 
for ex ls *.txt will match all files ending in .txt
* The ? 
* matches precisely one character
