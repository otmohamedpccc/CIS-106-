<<<<<<< HEAD
=======
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
* <!-- TOC -->autoauto- [Handling Text Files](#handling-text-files)auto    - [Grep command](#grep-command)auto    - [I/O redirection](#io-redirection)autoauto<!-- /TOC -->
* Paste command - join files horizontally in columns

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
* to get rid of Alias created, unalias
>>>>>>> 7575d03c9fa84dbaf3e28acaad08fd577b819fc6
