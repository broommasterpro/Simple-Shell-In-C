# A Simple Shell In C

A simple Unix shell built from scratch in C.

This project reads user input, tokenizes commands and arguments, executes built-in commands and launches external programs using Unix process management system calls.

### Overview
- Reads commands interactively from standard input.

- Tokenizes user input into commands and arguments.

- Supports built-in commands:
  - `cd`
  - `pwd`
  - `echo`
  - `help`
  - `exit`

- Executes external programs using `fork()` and `execvp()`.

- Waits for child processes using `waitpid()`.

- Dynamically allocates and resizes memory for input and command tokens.

- Handles invalid commands and system call errors.


## Dependencies

This project requires a Unix-like operating system and a C compiler.

Compile the project:

```bash
gcc shell.c -o shell
```


## Usage

Run the shell:

```bash
./shell
```

You will be presented with the shell prompt:

```text
>
```

Run built-in commands:

```bash
> pwd
> cd /path/to/directory
> echo hello world
> help
> exit
```

Run external programs:

```bash
> ls
> ls -l
> mkdir test
> cat file.txt
```
