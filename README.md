0x16. C - Simple Shell
Project to be done in teams of 2 people (your team: Benard Omoga, Tlhompho Moloi)

Background Context
Write a simple UNIX command interpreter.

Important message from Julien
It’s time for the famous Simple Shell project. This is one of the most anticipated project and also one that will challenge you a lot about everything you have learn so far:
Basics of programming
Basics of C
Basics of thinking like an engineer
Group work
and Learning how to learn
Resources
Read or watch:

Unix shell
Thompson shell
Ken Thompson
Everything you need to know to start coding your own shell concept page
man or help:

sh (Run sh as well)
Learning Objectives
At the end of this project, you are expected to be able to explain to anyone, without the help of Google:

General
Who designed and implemented the original Unix operating system
Who wrote the first version of the UNIX shell
Who invented the B programming language (the direct predecessor to the C programming language)
Who is Ken Thompson
How does a shell work
What is a pid and a ppid
How to manipulate the environment of the current process
What is the difference between a function and a system call
How to create processes
What are the three prototypes of main
How does the shell use the PATH to find the programs
How to execute another program with the execve system call
How to suspend the execution of a process until one of its children terminates
What is EOF / “end-of-file”?
List of allowed functions and system calls
access (man 2 access)
chdir (man 2 chdir)
close (man 2 close)
closedir (man 3 closedir)
execve (man 2 execve)
exit (man 3 exit)
_exit (man 2 _exit)
fflush (man 3 fflush)
fork (man 2 fork)
free (man 3 free)
getcwd (man 3 getcwd)
getline (man 3 getline)
getpid (man 2 getpid)
isatty (man 3 isatty)
kill (man 2 kill)
malloc (man 3 malloc)
open (man 2 open)
opendir (man 3 opendir)
perror (man 3 perror)
read (man 2 read)
readdir (man 3 readdir)
signal (man 2 signal)
stat (__xstat) (man 2 stat)
lstat (__lxstat) (man 2 lstat)
fstat (__fxstat) (man 2 fstat)
strtok (man 3 strtok)
wait (man 2 wait)
waitpid (man 2 waitpid)
wait3 (man 2 wait3)
wait4 (man 2 wait4)
write (man 2 write)
Compilation
Your shell will be compiled this way:

gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh

Tasks
0. Betty would be proud
	Write a beautiful code that passes the Betty checks

1. Simple shell 0.1
	Write a UNIX command line interpreter.

2. Simple shell 0.2
	Simple shell 0.1 +
	Handle command lines with arguments

3. Simple shell 0.3
	Simple shell 0.2 +
	Handle the PATH
	fork must not be called if the command doesn’t exist

4. Simple shell 0.4
	Simple shell 0.3 +
	Implement the exit built-in, that exits the shell
	Usage: exit
	You don’t have to handle any argument to the built-in exit

5. Simple shell 1.0
	Simple shell 0.4 +
	Implement the env built-in, that prints the current environment


6. Simple shell 0.1.1
	Simple shell 0.1 +
	Write your own getline function
	Use a buffer to read many chars at once and call the least possible the read system call
	You will need to use static variables
	You are not allowed to use getline
	You don’t have to:
	be able to move the cursor

7. Simple shell 0.2.1
	Simple shell 0.2 +
	You are not allowed to use strtok

8. Simple shell 0.4.1
	Simple shell 0.4 +
	handle arguments for the built-in exit
	Usage: exit status, where status is an integer used to exit the shell

9. setenv, unsetenv
	Simple shell 1.0 +
	Implement the setenv and unsetenv builtin commands

	setenv
	Initialize a new environment variable, or modify an existing one
	Command syntax: setenv VARIABLE VALUE
	Should print something on stderr on failure
	
	unsetenv
	Remove an environment variable
	Command syntax: unsetenv VARIABLE
	Should print something on stderr on failure


10. cd
Simple shell 1.0 +
Implement the builtin command cd:

Changes the current directory of the process.
Command syntax: cd [DIRECTORY]
If no argument is given to cd the command must be interpreted like cd $HOME
You have to handle the command cd -
You have to update the environment variable PWD when you change directory

11. ;
	Simple shell 1.0 +
	Handle the commands separator ;



12. && and ||
	Simple shell 1.0 +
	Handle the && and || shell logical operators

13. alias
	Simple shell 1.0 +
	Implement the alias builtin command
	Usage: alias [name[='value'] ...]
	alias: Prints a list of all aliases, one per line, in the form name='value'
	alias name [name2 ...]: Prints the aliases name, name2, etc 1 per line, in the form name='value'
	alias name='value' [...]: Defines an alias for each name whose value is given. If name is already an alias, replaces its value with value

14. Variables
	Simple shell 1.0 +
	Handle variables replacement
	Handle the $? variable
	Handle the $$ variable

15. Comments
	Simple shell 1.0 +
	Handle comments (#)

16. File as input
	Simple shell 1.0 +
	Usage: simple_shell [filename]
	Your shell can take a file as a command line argument
	The file contains all the commands that your shell should run before exiting
	The file should contain one command per line
	In this mode, the shell should not print a prompt and should not read from stdin






