#  MiniShell in C

This project is a simple command-line shell implemented in C. It supports standard system command execution, background process management, command chaining via pipes, and input/output redirection.

##  Features

* ✅ Execute system commands (`ls`, `cat`, `grep`, etc.)
* 🔁 Pipe support (`|`)
* 📂 Input/output/error redirection (`<`, `>`, `2>`)
* 🧵 Background processes (`&`) with job control
* ⚙️ Built-in commands:

  * `cd`: change directory
  * `jobs`: view background processes
  * `fg`: bring background job to foreground
  * `salir`: exit the shell

## Compilation and Execution

### Requirements

* `gcc` compiler
* Linux-based environment

### Steps

```bash
gcc minishell.c -o minishell
./minishell
```

##  Usage Examples

```bash
msh > ls -l | grep .c > output.txt
msh > cat < input.txt | sort | uniq > result.txt &
msh > jobs
msh > fg 1
msh > cd /home/user
msh > salir
```

## ⚙️ Technologies

* C programming language (C99)
* System calls: `fork`, `execvp`, `pipe`, `dup2`, `waitpid`, `open`, `close`

