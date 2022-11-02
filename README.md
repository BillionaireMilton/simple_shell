0x16. C - Simple Shell
     _____       _                     __    _____ _          _ _ 
    / ____|     | |                   / _|  / ____| |        | | |
   | |  __  __ _| |_ ___  ___    ___ | |_  | (___ | |__   ___| | |
   | | |_ |/ _` | __/ _ \/ __|  / _ \|  _|  \___ \| '_ \ / _ \ | |
   | |__| | (_| | ||  __/\__ \ | (_) | |    ____) | | | |  __/ | |
    \_____|\__,_|\__\___||___/  \___/|_|   |_____/|_| |_|\___|_|_|
The Gates of Shell by Milton , featuring Somebody

Resource
* Unix shell
* Thompson shell
* Ken Thompson
* Everything you need to know to start coding your own shell

List of allowed functions and system calls
* access (man 2 access)
* chdir (man 2 chdir)
* close (man 2 close)
* closedir (man 3 closedir)
* execve (man 2 execve)
* exit (man 3 exit)
* \_exit (man 2 _exit)
* fflush (man 3 fflush)
* fork (man 2 fork)
* free(man 3 free)
* getcwd (man 3 getcwd)
* getline (man 3 getline)
* getpid (man 2 getpid)
* isatty (man 3 isatty)
* kill (man 2 kill)
* malloc (man 3 malloc)
* open (man 2 open)
* opendir (man 3 opendir)
* perror (man 3 perror)
* read (man 2 read)
* readdir (man 3 readdir)
* signal (man 2 signal)
* stat (__xstat) (man 2 stat)
* lstat (__lxstat) (man 2 lstat)
* fstat (__fxstat) (man 2 fstat)
* strtok (man 3 strtok)
* wait (man 2 wait)
* waitpid (man 2 waitpid)
* wait3 (man 2 wait3)
* wait4 (man 2 wait4)
* write (man 2 write)
The shell will be compiled this way:
$ gcc -Wall -Werror -Wextra -pedantic -std=gnu89 \*.c -o hsh

Output
* Unless specified otherwise, your program must have the exact same output as sh (/bin/sh) as well as the exact same error output.
* The only difference is when you print an error, the name of the program must be equivalent to your argv[0] (see below)
Example of error with sh:
$ echo "qwerty" | /bin/sh
/bin/sh: 1: qwerty: not found
$ echo "qwerty" | /bin/../bin/sh
/bin/../bin/sh: 1: qwerty: not found
$
Same error with your program hsh:
$ echo "qwerty" | ./hsh
./hsh: 1: qwerty: not found
$ echo "qwerty" | ./././hsh
./././hsh: 1: qwerty: not found
$

Testing
The shell should work like this in interactive mode:
$ ./hsh
($) /bin/ls
hsh main.c shell.c
($)
($) exit
$
But also in non-interactive mode:
$ echo "/bin/ls" | ./hsh
hsh main.c shell.c test\_ls\_2
$
$ cat test\_ls\_2
/bin/ls
/bin/ls
$
$ cat test\_ls\_2 | ./hsh
hsh main.c shell.c test\_ls\_2
hsh main.c shell.c test\_ls\_2
$

Features
* To add as we progress

Builtins
* To add as we progress

Authors
* Milton Jesumbo
