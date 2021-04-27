* mv command moves data from one file to another
\ makes it as one word - 'escapes a character'
ex mv ~/download/topics\ to\ study\ midterm.md ./
./ represents current directory
/ means root 
absolute path - is the full address to a file 
* double quotes escape characters 
* to rename mv file1.txt new_file1.txt

## Grep command 
used to match a string pattern from a file or a standard output when using the pipe
* Usage: grep + option + pattern to match file
* standard output+pipe (|) + grep + pattern to match 
* grep - 'grab'
* grep -i turns case sens. off
* grep -n Displays line number of each line matched
* grep -E treats the pattern as an extended_regular_expression grep -V Inverts the search
* grep -l
* grep -o only display the string matched 

* ex. grep -n Linux topics.md - is highlighting linux bc thats what were looking for.
* /etc/passwd displays 7 fields 

shell is a program that provides access to the linux system

cut command 
* Cut command - extracts specific sections of lines of a file and display it to the screen
* c
* the limiter is any character that allows you to divide file into columns
* ex cut + option + file 
* cut -f1 displays the fist field of each line, using : as the field separator 
* etc/passwd contains all users
* cut -d : -f1 /etc/passwd displays the first field of each line, using: as the field separator 
*  :  the delimeter is a character that separates separate strings 
*  to save input 'command' > 'filename'

* > to save to a file 
* >> to append a file 
* --output-delimeter=' = '
* cut -d ' ' -f1 file 
* a space is a character 

* curl - run a script     curl | bash 
* wget - download a file 

* mkdir -P school/pccc/{old,new} - creates , parent and sub directories 

* inode - the number id of a file 
* you can ls absolute paths and relative  