# Linux File permissions 

* a file can be owned by only one user 
* ls -l shows you the file user owner and group owner 
* the /etc/passwd file contains a list of all users in linuc 
* /etx/group 

* chown command is used for changing grpu owner
* syntax: chown user:group file 

    * Ex: chown john file.txt
  
permission groups User Guest Other 

* Files 
* R (read)- gives users permission to open a file and view its contents 
* W (write)- gives useers permission to open a file and edit its contents 
* X (execute)- Allows users to run the file (as long as its a program or script) 

* Directories
* R allows users to list a directorys content with commands such as ls 
* w allows user to add or remove files and subdirectories 
* X allows users to switch to the directory with the cd command 
a hyphen (-) indicates user doesnt have certain permission


* chmod command is used to change permission on files and directories 
* syntax: chmod permissions file/directory 
* can use chmod command in two ways to change file permissions 

* Symbolic notation 
* permissions applied using symbols 

Category| Operator | permission 
u ( user ) | + add to existing 
g ( group) | - remove from existing 
o (other)  |
a (all) 

Numeric Notation 
--- o 
--x 1 
-w- 2 
-wx 3
r-- 4
r-x 5
rw- 6
rwx 7

Permission 
Read - 4 
Write - 2 
execute - 1



