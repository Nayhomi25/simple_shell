# Simple Shell

## Table of Contents
* [Introduction](#Introduction)
	* Goal
	* What is Shell
* [Project Requirement](#Project-Requirement)
	* General
	* Allowed functions and system calls
	* General requirements
	* Allowed functions
* [Project Information](#Project-Information)
	* Tasks
* [Documentation](#Documentation)
	* Installation
	* Running
	* Files

## Introduction

### Goal
The goal of this project is simply to understand how shell works and also being able to write scripts that interacts with the shell

### What is Shell
A **shell** is a command-line interpreter. It is  computer program that exposes an operating system's services to a users or programs residing in a computer.

## Project Requirements

### General
- Allowed editors: vi, vim, emacs
- All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
- All your files should end with a new line
- A README.md file, at the root of the folder of the project is mandatory
- Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
- Your shell should not have any memory leaks
- No more than 5 functions per file
- All your header files should be include guarded
- Use system calls only when you need to (why?)
- Write a README with the description of your project
- You should have an AUTHORS file at the root of your repository, listing all individuals having contributed content to the repository. Format, see Docker

### Allowed functions and system calls

- access (man 2 access)
- chdir (man 2 chdir)
- close (man 2 close)
- closedir (man 3 closedir)
- execve (man 2 execve)
- exit (man 3 exit)
- _exit (man 2 _exit)
- fflush (man 3 fflush)
- fork (man 2 fork)
- free (man 3 free)
- getcwd (man 3 getcwd)
- getline (man 3 getline)
- getpid (man 2 getpid)
- isatty (man 3 isatty)
- kill (man 2 kill)
- malloc (man 3 malloc)
- open (man 2 open)
- opendir (man 3 opendir)
- perror (man 3 perror)
- read (man 2 read)
- readdir (man 3 readdir)
- signal (man 2 signal)
- stat (__xstat) (man 2 stat)
- lstat (__lxstat) (man 2 lstat)
- fstat (__fxstat) (man 2 fstat)
- strtok (man 3 strtok)
- wait (man 2 wait)
- waitpid (man 2 waitpid)
- wait3 (man 2 wait3)
- wait4 (man 2 wait4)
- write (man 2 write)

## Project Information

### Tasks
- Task 0. Betty would be proud: a code that passes the Betty checks.
- Task 1. Simple shell 0.1: a UNIX command line interpreter.
- Task 2. Simple shell 0.2: Handle command lines with arguments.
- Task 3. Simple shell 0.3: Handle the PATH and calls fork if the command doesn’t exist.
- Task 4. Simple shell 0.4: Implement the exit built-in, that exits the shell.
- Task 5. Simple shell 1.0: Implement the env built-in, that prints the current environment.
- Task 6. Simple shell 0.1.1: My own getline function.
- Task 7. Simple shell 0.2.1: Simple shell 0.2 + (You are not allowed to use strtok).
- Task 8. Simple shell 0.4.1: Simple shell 0.4 + (handle arguments for the built-in exit).
- Task 9. setenv, unsetenv: Implement the setenv and unsetenv builtin commands.
- Task 10. cd: Implement the builtin command cd.
- Task 11. ;: Handle the commands separator ;.
- Task 12. && and ||: Handle the && and || shell logical operators.
- Task 13. alias: Implement the alias builtin command.
- Task 14. Variables: Handle variables replacement. Handle the $? variable and Handle the $$ variable.
- Task 15. Comments: Simple shell 1.0 + (Handle comments (#)).
- Task 16. File as input: Simple shell 1.0 + (Usage: simple shell _filename_. Shell can take a file as a command line argument, this file contains all the commands that your shell should run before exiting, contain one command per line, the shell should not print a prompt and should not read from stdin).

## Documentation

### Installing
Perform the following tasks in order to run this program

- Clone This Repo: `` https://github.com/Nayhomi25/simple_shell.git ``
- Navigate into this repository: `cd simple_shell`
- compile: it with  `gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh`
- Run the shell in interactive mode or non interactive mode: `./hsh` or `command | ./hsh`

### Running
To run this program, first compile it, then execute it with the following command:
`$ ./hsh`
The prompt below would be displayed, indicating commands can be entered.
`$ `

Example:
```
$ ./hsh
$
$ ls -l
.
.
.
```
### Files

|File|Description|
|---|---|
|[AUTHORS](https://github.com/Nayhomi25/simple_shell/blob/main/AUTHORS)|Contributors in this repository|
|[README.md](https://github.com/Nayhomi25/simple_shell/blob/main/README.md)|Information about our repository|
|[alias.c](https://github.com/Nayhomi25/simple_shell/blob/main/alias.c )|Implements alias builtin commands|
|[args.c](https://github.com/Nayhomi25/simple_shell/blob/main/args.c)|Get command from standard input|
|[builtins.c](https://github.com/Nayhomi25/simple_shell/blob/main/builtins.c)|Matches command wih corrsponding shell builtin|
|[alias2.c](https://github.com/Nayhomi25/simple_shell/blob/main/alias2.c)|Implements alias builtin command|
|[environs.c](https://github.com/Nayhomi25/simple_shell/blob/main/environs.c)|Handles environment variable related tasks|
|[error.c](https://github.com/Nayhomi25/simple_shell/blob/main/error.c)|Creates error message|
|[function.c](https://github.com/Nayhomi25/simple_shell/blob/main/function.c)|Handles PATH|
|[getline.c](https://github.com/Nayhomi25/simple_shell/blob/main/getline.c)|Custom getline function|
|[handles.c](https://github.com/Nayhomi25/simple_shell/blob/main/handles.c)|checks line for logical operators _OR_ and _AND_|
|[helpmsg.c](https://github.com/Nayhomi25/simple_shell/blob/main/helpmsg.c)|Displays help message|
|[helpmsg2.c](https://github.com/Nayhomi25/simple_shell/blob/main/helpmsg2.c)|More implimentation code for help message|
|[main.h](https://github.com/Nayhomi25/simple_shell/blob/main/main.h)|Main header file|
|[shell.c](https://github.com/Nayhomi25/simple_shell/blob/main/shell.c)|Calls shell prompt|
|[strhelp.c](https://github.com/Nayhomi25/simple_shell/blob/main/strhelp.c)|Performs operation on strings|
|[tokens.c](https://github.com/Nayhomi25/simple_shell/blob/main/tokens.c)|Performs operation token related operations|
|[var.c](https://github.com/Nayhomi25/simple_shell/blob/main/var.c)|Handles variable replacemants|
|[2-strhelp.c](https://github.com/Nayhomi25/simple_shell/blob/main/2-strhelp.c)|Locate characters in strings|
|[builtin2.c](https://github.com/Nayhomi25/simple_shell/blob/main/builtin2.c)|Print current environment|
