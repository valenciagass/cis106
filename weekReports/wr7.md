---
name: Valerie Pallares
semester: Fall 23
course: cis106
---

# Week Report 7

## Handling Textfiles.

### cat command
* What is the command used for?
    * used for displaying the content of a file. 

* What is the formula of the command
    * cat +option +file/s to display

###### Examples of using the command:
##### Display the content of a file located in the pwd
    * cat todo.list
##### Display the content of a file using absolute path
    * car ~/Documents/todo.lst

### tac command
* What is the command used for?
    * displaying the content of a file in a reverse order

* What is the formula of the command
    * tac + option +file/s to display

###### Examples of using the command:
##### Dispplay the content of a file located in the pwd
    * tac todo.md
##### Display the content of a file using absolute path
    * tac ~Documents/todo.md
  
### head command
* What is the command used for?
    * display the top N number of lines of a given file. by default, it prints out the first 10 lines. 

* What is the formula of the command
    * head + option +file/s

###### Examples of using the command:
##### Display the first 10 lines of a file
    * head ~/Documents/Book/dracula.txt
##### Display the first 5 lines of a file
    * head -5 ~/Documents/Book/dracula.txt

### tail command
* What is the command used for?
    * displays the N number of lines of a given file. By default, it prints the last 10 lines

* What is the formula of the command
    * tail + option + file
    * 
###### Examples of using the command:
##### Display the last 10 lines of a file
     * tail ~/Documents/Book/dracula.txt
##### Display the last 5 lines of a file
     * tail -5 ~/Documents/Book/dracula.txt

### cut command
* What is the command used for?
    * used to extract a specific section of each line of a file and display it to the screen

* What is the formula of the command
    * cut + option + file/s

###### Examples of using the command:
##### Display a list of all the users in your system
    * cut -d ':' -f1 /etc/passwd
##### Display a list of all the users in your system with their login shell
    * cut -d ':' -f17 /etc/passwd
  
### paste command
* What is the command used for?
    * used for joining files horizontally in columns

* What is the formula of the command
    * paste + option + files

###### Examples of using the command:
##### Merge two files
    * paste users.lst ip_address .lst
##### Merge two files using a different delimiter
    * paste -d ":' users1.lst ip_addresses.lst

### sort command
* What is the command used for?
    * used for sorting files alphabetically, in reverse order, by number and by month

* What is the formula of the command
    * sort + option +file
    
###### Examples of using the command:
##### Sort a file
    * sort users.lst
##### Sort a file by column number
    * sort -k 2 users.txt

### wc command
* What is the command used for?
    * used for printing the number of lines, characters and bytes in a  file

* What is the formula of the command
    * wc + option + file/s

###### Examples of using the command:
##### Display the number of characters in a file
    * wc -m users.txt
##### Display the number of lines in a file
    * wc -l users.txt

### tr command
* What is the command used for?
    * used for translating or deleting characters from standard point

* What is the formula of the command
    * standard output | tr +option + set + set

###### Examples of using the command:
##### Translate one character to another (a period with a comma)
    * cat file.txt | tr '.' ','
##### Translate tabs into space
    * cat file.py | tr -s "[:space:]" '/t'

### diff command
* What is the command used for?
    * compares files and displays the differences between them

* What is the formula of the command
    * diff + option + file1 +file2

###### Examples of using the command:
##### Display the difference between two files 
    * diff cars. csv cars-backup.csv
##### Display the difference between two files in a column format:
    * diff -y cars. csv cars-backup.csv


### grep command
* What is the command used for?
    * to search text in a given file.

* What is the formula of the command
    * grep + option + search criteria + file/s

###### Examples of using the command:
##### Search any lines that contains the word "dracula" in the given file
    * grep 'dracula- ~Documents/dracula.txt
##### Search and match only the word
    * grep -o 'dracula ~/Documents/Books/dracula.txt

### awk command
* What is the command used for?
    * a scripting language used for processing and displaying text. 

* What is the formula of the command
    * awk + options + {awk command} + file + file to save (optional)

###### Examples of using the command:
##### Print the first column of every line of a file
    * awk {print $1} ~/Documents/Csv/cars.csv
##### Print first field of /etc/passwd
    * awk -F: '{print$1}' /etc/passwd
##### Print the last field of the /etc/passwd file
    * awk -F: '{print $NF} /etc/passwd
##### print the first and last field of the /etc/passwd
    * awk -F: '{print $1," = ", $NF} /etc/passwd
##### Print the first and 3 fields with line numbers
    * awk -F: '{print NR,$1,$3}' /etc/passwd

### sed command 
* What is the command used for?
    * a stream editor that performs operations on files and standard output. 

* What is the formula of the command:
    * sed options + sed script + file

###### Examples of using the command
##### Replacing a string in given file (replace pizza for rice)
    * sed 's/pizza/rice/' shopping-list.lst
##### Replacing the number of occurrences of a pattern ina  file 
    * sed 's/pizza/rice/4' shopping-list.lst
##### Replacing all the occurrences of the pattern in a file
    * sed 's/pizza/rice/g' shopping-lst.lst
##### Replacing string on a specific line number 
    * sed '3 s/pizza/rice/' shopping-list.txt
##### Replacing string on a range of lines 
    * sed '1,3 s/pizza/rice/' shopping-list.lst
