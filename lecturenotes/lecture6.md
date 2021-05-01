**lecture 5 Notes for hw is here**
.odt - libreoffice - problematic on windows , little bit on apple pages bc not good 

plain text - text that is not computationally tagged, specially formatted, or written in code.
formatted text - written in special style/characters 

**nano** - default text editor of GNU 
very limited text editor 

**VIM**
Vim command line text editor is included in all POSIX compliant OS 
learning vi takes tgiome 
crucial for system administration 
not included in Ubuntu 
tin install - sudo apt install vim 

**how to start and quit vim**
to start type: vim     
to exit - hit esc then type :qa! then press enter 
to exit - q<Enter> to exit 
to help - help<Enter> kfor <F1> for online help

: > prefix for entering command line mode 
q > short for quit 
a > short for all buffers
! > force 
:qa! > close all 

* Insert mode - used for wirting txt 
* Normal mode used for manipulatng text 
* Command mode used to type vim commands 
* visual mode similar to visual mode 
* select mode similar to visual - used for processing a bunch of lines in one shot 
* EX- mode 
when you start vim you're automatically in  Normal mode 
press letter i - insert mode 

**Navigating a File** 
* H = left
* J = down 
* K = up
* L = right 

**saving and quitting vim** 
* to save a text file you need to enter normal mode using :w 
* :w will save the file 
* :w new.txt will save file as new.txt
* :wq will save file and quit 
* :wqa! will save file and close all 

**editing a file with vim**
* :e new,txt -> will open new.txt and allow you to edit 
* you can use autocompletion 
* Ctrl + g will show the file that you are currently editing in the status line 
* you can also use the "f in command mode to see the file that you are currently working on 

**searching words in vim**
Use / and the word you are looking for 
    for ex /hello 
? to search backward
    ?hello 
* '*' will search for the next occurrence of the word under the cursor 
* '#' will  search for the previous occurrence of the word under the cursor

**screen movement** 
G - moves to end of file 
gg moves to begginning 
CTRL -f forward
CTTRL - b moves a page backward at a time 
to move multipl pages at a time write the number in front 
    * 2 ctrL f 

**moving to lines**
:set nu - sets line numbers 
use : plus the line number 
    * for ex :* will move you to line 8
    * additionally use 8G
*  $ will move to the end of the line 
*  O will move to beginning of the line 
*  vim sample.txt +100 will open sample.txt and move to line 100
* '+' executes any vim command from the shell prompt 

**Delete text and copy and paste**
* dw - delete current word
* u - undo 
* dd - delete line under the cursor 
* d + /word - delete until word given 
* yw - copy the current word 
* p - for paste after the cursor 
* P - for paste before the cursor 
* yy - copies a whole line 
* x - cut 

**change text** 
cw - deletes the word under the cursor and enters insert mode 
c /hello - deletes until it finds the word hello and enters insert mode 
* Visual Selection
  * SHIFT + V select lines 
  * CTRL + V select blocks 
* Replace text 
* :s/old word/new word will replace all the word with the give one 
* :s/old/new - will replace the first occurrence of the word old
* :%s/old/new/g - replace all the occurrences of the word old 
* :s/old/new/g/y - will ask you 

**work in split screen mode** 
to open a new VIM window next to current one - CTRL + w then v
* to open a new windo below current - CTRL +w the s
* to move to the window on the right/left/down/up
* CTRL + w then h/l/j/k

**useful to know** 
read files - SHFIT + o - enters a new empty line 
create a vim custom file 
    in yopur home dierectory create a file named .vimrc and add the commands to that file - http://learnvimscriptthehardway.stevelosh.com/
Run an external command - :!+command

run a command and paste file
    :r!+command
# Managing Data
  archive - file containing many other fields of each which is still identified by it filename

  * backup- copies files and directories to an archive 
  * system backup - use to restore data in case of a system failure or data loss and corruption 
**List of important directories**
 * /etc - contains core configure files, security files, network configuration files, user and group information, etc
 * /home- each user has a /home directory 
 * /opt - software and packages added after the default installation 
 * /root - root users home directory
 * /var - system specific information that changes while the system is running normally 

**archiving utilities** 
* Tar (tape archive): creates archives by combining files and directortires into a single file 
* files created with tar must end in .tar
* To create an archive
  + tar + options + archive name + files to add to archive 
  
* To extract an archive**-
  
 + tar + options + file to extract 
  
 + -c or --create - creates an archive file 
  
 + -t or --list - lists an archives contents
  
 + -x or --extract - extracts archives contents 

 + -f or --file  - specifies the archive files name and location (command is always required) 
  
 + -v or --verbose - displays details about copying files to and extracting files from archives 
  
 + -z or ---gzip, --ungzip - filters an archive through gzip
  
 + -J - decompresses

 + -r inserts a file into the archive
  
 + -d decompresses archives

example - tar -cf myfiles.tar ~/Downloads/* ~/Pictures/* (used * wildcard to extract all files *.{jpeh,png,pdf} 
a file thats inside an archive is called a member 

* cpio command 
* The option to create an archive is -o
  * ls | cpio -ov > arcive.cpio 
* To extract an archive to cpio use the -i option with < 
  * cpio -iv < archive.cpio 
* Archive specific files 
  * find / -iname *.sh | cpio -ov > scriptsArchive.cpio

# File Compression 
Og , UNIX file compression was handled by a utlity called compress 
compress was pateneted and most people staertr using a different utility 
Gzip (GNU Zip) 
gzip, bzip2, xz compress files in place meaning the og file is deleted after compression
bzip2 offers better compression ratios than gzip 
xz is better than both 
gzip is not a replacement for zip 
* compress a file - xz file.txt
* compress mult. files - gzip file1.txt file2.txt file3.txt

