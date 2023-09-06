# Our own simple shell

This is our self owned simple shell in C language.

### About

Shell is a user interface to use the services of a computer. It can be a command-line interface –the one we will build- or graphical user interface, like regular software such as Windows Office.

### Compilation
This simple shell is compiled with:
```
gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh
```

### Output
This program have exact same output as ```sh``` as well as the exact same error output. The only difference is when it prints an error, the name of the program is equivalent to ```argv[0]```.

#### Example of error with ```sh```:
```
$ echo "qwerty" | /bin/sh
/bin/sh: 1: qwerty: not found
$ echo "qwerty" | /bin/../bin/sh
/bin/../bin/sh: 1: qwerty: not found
$
```

#### Error with our program:

```
$ echo "qwerty" | ./hsh
./hsh: 1: qwerty: not found
$ echo "qwerty" | ./././hsh
./././hsh: 1: qwerty: not found
$
```
### Testing
#### Our shell work like this in interactive mode:
```
$ ./hsh
($) /bin/ls
hsh main.c shell.c
($)
($) exit
$
```

#### But also in non-interactive mode:
```
$ echo "/bin/ls" | ./hsh
hsh main.c shell.c test_ls_2
$
$ cat test_ls_2
/bin/ls
/bin/ls
$
$ cat test_ls_2 | ./hsh
hsh main.c shell.c test_ls_2
hsh main.c shell.c test_ls_2
$
```
### Examples
```
$ /bin/pwd
/home/wiseman/simple_shell
```

```
$ ls -la
total 85
drwxrwxrwx 1 Yuntech1   512 Sep 19 15:02 .
drwxr-x--- 1 Yuntech1  512 Sep 19 14:23 ..
drwxrwxrwx 1 Yuntech1  512 Sep 19 14:23 .git
-rw-rw-rw- 1 Yuntech1  3456 sep 19 15:03 README.md
-rw-rw-rw- 1 Yuntech1   858 sep 19 14:18 _setenv.c
-rw-rw-rw- 1 Yuntech1  1251 sep 16 23:50 _strtok.c
-rw-rw-rw- 1 Yuntech1   434 sep 19 10:58 _unset.c
-rwxrwxrwx 1 Yuntech1 17648 sep 19 08:53 a.out
-rw-rw-rw- 1 Yuntech1   536 sep 19 14:09 break_input.c
-rw-rw-rw- 1 Yuntech1   563 sep 19 14:45 checkargs.c
-rw-rw-rw- 1 Yuntech1   231 sep 19 10:39 environ.c
-rw-rw-rw- 1 Yuntech1   537 sep 19 14:16 execute.c
-rw-rw-rw- 1 Yuntech1   356 sep 19 14:13 exit_com.c
-rw-rw-rw- 1 Yuntech1  268 sep 19 07:49 free_buff.c
-rw-rw-rw- 1 Yuntech1  500 sep 19 14:14 handle_comment.c
-rw-rw-rw- 1 Yuntech1  430 sep 19 08:51 handle_coms.c
-rwxrwxrwx 1 Yuntech1 17664 sep 19 14:43 hsh
-rw-rw-rw- 1 Yuntech1 main.c
-rw-rw-rw- 1 yuntech 1   702  main.h
```

```
$ Ethio
./hsh: No such file or directory
```

### Authors
[Olayiwola Yunus Abayomi](https://github.com/Yuntech1)
[Gabriel ekong](https://github.com/Gabriel ekong)
