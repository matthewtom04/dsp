# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

1) pwd - show current working directory path
2) mkdir - creating a directory
3) rmdir - deleting a directory
4) touch < filename > - creating a file using 'touch' command
5) rm - deleting a file
6) mv - renames/move file
7) ls - a - lists all the hidden files
8) cp - copying a file from one director to another
9) wc - tells you how many lines and characters are in the file
10) cd - returns to home directory



---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

1) ls - list files
2) ls - a - list all of the hidden files
3) ls - l - lists all the details of the file ('long format')
4) ls -lh - lists all files in long format and by size.
5) ls -lah - lists all files and hidden files in long format and the size of the file.
6) ls -t - sorts list by time
7) ls -Glp - Shows a list that enables color, lists in long format, and writes a slash ('/') after every directory.

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

My favorite commands are:
1) ls -la
2) ls - u
3) ls -g 
4) ls -d
5) ls -ac


---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

xargs - is a command that builds and execute commands from standard inputs.
example:
echo 'one two three' | xargs mkdir - makes directorys 'one','two', and 'three'.

 

