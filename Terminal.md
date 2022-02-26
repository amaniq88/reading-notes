## Linux Tutorial - 1. The Command Line

A command line, or terminal, is a text based interface to the system.

## Linux Tutorial - 2. Navigation

pwd
Print Working Directory - ie. Where are we currently.
ls
List the contents of a directory.
cd
Change Directories - ie. move to another directory.

Relative path
A file or directory location relative to where we currently are in the file system.
Absolute path
A file or directory location in relation to the root of the file system.

## Linux Tutorial - 3. More About Files
- Everything is a File , the behaviour of Linux as we manage files and directories.
- Linux the system actually ignores the extension and looks inside the file to determine what type of file it is.
`file [path]`
obtain information about what type of file a file or directory is.
- Linux is Case Sensitive
- to use spaces in the file name we use , Quotes "" ''  or Escape Characters / 
- If the file or directory's name begins with a . (full stop) then it is considered to be hidden
`ls -a`
List the contents of a directory, including hidden files.

## Linux Tutorial - 4. Manual Pages
The manual pages are a set of pages that explain every command available on your system including what they do, the specifics of how you run them and what command line arguments they accept.
- man <command>
Look up the manual page for a particular command.
- man -k <search term>
Do a keyword search for all manual pages containing the given search term.
- /<term>
Within a manual page, perform a search for 'term'
- n
After performing a search within a manual page, select the next found item.

## Linux Tutorial - 5. File Manipulation
- mkdir
Make Directory - ie. Create a directory.
- rmdir
Remove Directory - ie. Delete a directory.
- touch
Create a blank file.
- cp
Copy - ie. Copy a file or directory.
- mv
Move - ie. Move a file or directory (can also be used to rename).
- rm
Remove - ie. Delete a file.


## Linux Tutorial - 6. Vi Text Editor

No mouse
vi is a text editor where everything is done on the keyboard. If you can touch type then this is great. If not then maybe you should think about learning.
Edit commands
There are many of them. Practice is the key to remember the most commonly used and useful ones.

- vi
Edit a file.
- cat
View a file.
- less
Convenient for viewing large files.


## Linux Tutorial - 7. Wildcards
Wildcards are a set of building blocks that allow you to create a pattern defining a set of files or directories. 

the basic set of wildcards:

- (*) represents zero or more characters
- ? - represents a single character
- [] - represents a range of characters

## Linux Tutorial - 8. Permissions
Linux permissions dictate 3 things you may do with a file, read, write and execute. They are referred to in Linux by a single letter each.

- r read - you may view the contents of the file.
- w write - you may change the contents of the file.
- x execute - you may execute or run the file if it is a program or script.

For every file we define 3 sets of people for whom we may specify permissions.

- owner - a single person who owns the file. (typically the person who created the file but ownership may be granted to some one else by certain users)
- group - every file belongs to a single group.
- others - everyone else who is not in the group or the owner.

Command :
- chmod
Change permissions on a file or directory.
- ls -ld
View the permissions for a specific directory.

## Linux Tutorial - 9. Filters
A filter, in the context of the Linux command line, is a program that accepts textual data and then transforms it in a particular way. Filters are a way to take raw data, either produced by another program, or stored in a file, and manipulate it to be displayed in a way more suited to what we are after.

commands :
- head
View the first n lines of data.
- tail
View the last n lines of data.
- sort
Organise the data into order.
- nl
Print line numbers before data.
- wc
Print a count of lines, words and characters.
- cut
Cut the data into fields and only display the specified fields.
- sed
Do a search and replace on the data.
- uniq
Remove duplicate lines.
- tac
Print the data in reverse order.

## Linux Tutorial - 10. Grep and Regular Expressions
Regular expressions are similar to the wildcards . They allow us to create a pattern. typically used to identify and manipulate specific pieces of data.

`egrep -- 
View lines of data which match a particular pattern.`


## Linux Tutorial - 11. Piping and Redirection
Every program you may run on the command line has 3 streams, STDIN, STDOUT and STDERR.
- ->
Save output to a file.
- ->>
Append output to a file.
- -<
Read input from a file.
- -2>
Redirect error messages.
- |
Send the output from one program as input to another program.

## Linux Tutorial - 12. Process Management
A program is a series of instructions that tell the computer what to do. When we run a program, those instructions are copied into memory and space is allocated for variables and other stuff required to manage its execution. This running instance of a program is called a process and it's processes which we manage.

- top
View real-time data about processes running on the system.
- ps
Get a listing of processes running on the system.
- kill
End the running of a process.
- jobs
Display a list of current jobs running in the background.
- fg
Move a background process into the foreground.
- ctrl + z
Pause the current foreground process and move it into the background.


## Linux Tutorial - 13. Bash Scripting
A Bash script allows us to define a series of actions which the computer will then perform without us having to enter the commands ourselves. If a particular task is done often, or it is repetetive, then a script can be a useful tool.

A Bash script is interpreted (read and acted upon) by something called an interpreter. There are various interpreters on a typical linux system but we have been learning the Bash shell so we'll introduce bash scripts here.
