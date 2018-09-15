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

> > pwd: Show current working directory path
    mkdir: Create a directory
    rm -r: Delete a directory
    touch: Create a file
    rm: Delete a file
    mv: Rename a file
    ls -a: List all files, including hidden files
    cp: Copy a file from one directory to another
    grep: Searches file for lines that match input and returns them
    sort: Sorts the contents of the input in alphabetical order
    

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

> > `ls`: Displays all unhidden contents in the directory that match name inputted (will return all files if no argument)
    `ls -a`: Displays contents in the directory, including hidden contents
    `ls -l`: Displays contents in the directory in long form
    `ls -lh`: Displays contents in the directory in long form with human-readable file sizes
    `ls -lah`: Displays contents in the directory, including hidden contents, in long form with human-readable file sizes
    `ls -t`: Displays contents in the directory sorted in reverse chronological order
    `ls -Glp`: Displays contents in the directory in long form with the "/" character after directories and with colored output

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > 'ls -d': Displays only directories in the directory
    'ls -m': Displays contents as part of a comma separated list
    'ls -r': Displays contents in reverse order
    'ls -u': Displays files by file access time
    'ls -1': Displays entry on one line

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > The 'xargs' command takes standard input and converts it to arguments for a command. An example of how to use this is: 
      echo "test 123" | xargs mkdir
    which creates a directory called "test 123", the output of echo.

 

