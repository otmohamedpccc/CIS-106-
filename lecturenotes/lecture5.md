# Handling Text Files 
* CAT command
  * concatenate - to join two strings together, two files together, two texts together
  * CAT + (a single file) =  list content of the single file 
  * cat -n to view line numbers 
  * cat -b to display content of file with line numbers excluding empty lines.
  * cat -E displays $ at end of every line so you know where the end of the line is 

* TAC command 
* works like cat but displays list from bottom to top 

* More command
  * a pager program used for displaying the context of text files one page at a time
  * more -d open a file and display guding info in the bottom 
  * more -10 open a file 10 lines at a time 

* Less command - faster than more 
* les -N to file a line 

* Head command - displays the top N number of lines 

* Cut command - extracts specific sections of lines of a file and display it to the screen
* cut -b 
* the limiter is any character that allows you to divide file into columns
* ex cut + option + file 
* cut -f1 displays the fist field of each line, using : as the field separator 
* etc/passwd contains 
* cut -d : -f1 /etc/passwd displays the first field of each line, using: as the field separator 
* ex cut -d '-' f1 
* 
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

* Grep command 