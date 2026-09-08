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

## Iforgot
 
'Iforgot' is a helper tool meant for when you can't exactly remember what command to use or how to use a particular command and don't have the energy to go through the man page. 

### Example
 
```text
> Iforgot rename
How can I rename?
1. mv original_name new_name
 
> Iforgot delete
How can I delete?
1. rm file_to_delete
2. rm -r directory_to_delete
3. rm -f force_delete_file
```
 
Supported actions: `rename`, `copy`, `delete`, `move`, `compress`, `extract`, `search`, `find`, `view`, `edit`, `create`, `list`, `permissions`, `download`, `count`, `compare`, `link`, `disk`, `kill`, `processes`, `network`, `history`. I plan on adding more commands in the future `:)`
