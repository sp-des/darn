# darn

Prints a helpful message in the terminal for when you can't remember commands. (family friendly)


### Extremely helpful

People all around the the world find this useful.

> "This useful program helped me stay calm when i couldn't remember commands for the terminal. Good to see programmers programming useful things again!" - Leonardo Da Vinci

### How to incorporate it into your life

1. Download the software
2. Open a terminal to the location of the software and copy and paste this into the terminal: `chmod +x darn`
3. Now copy the software in the path, /usr/bin, like this: `cp darn /usr/bin/`

You're all done! Now you can run this super helpful and realistic software by typing the script name! 


## Documentation 

### Shell Commands
A simple shell command such as `echo a b c` consists of the command itself followed by arguments, separated by spaces.

More complex shell commands are composed of simple commands arranged together in a variety of ways: in a pipeline in which the output of one command becomes the input of a second, in a loop or conditional construct, or in some other grouping.

### Simple Commands
A simple command is the kind of command encountered most often. It’s just a sequence of words separated by `blank`s, terminated by one of the shell’s control operators. The first word generally specifies a command to be executed, with the rest of the words being that command’s arguments.

The return status of a simple command is its exit status as provided by the POSIX 1003.1 `waitpid` function, or 128+n if the command was terminated by signal n.

### Pipelines
A `pipeline` is a sequence of one or more commands separated by one of the control operators ‘|’ or ‘|&’.

The format for a pipeline is:

> [time [-p]] [!] command1 [ | or |& command2 ] …

The output of each command in the pipeline is connected via a pipe to the input of the next command. That is, each command reads the previous command’s output. This connection is performed before any redirections specified by the command.

If ‘|&’ is used, command1’s standard error, in addition to its standard output, is connected to command2’s standard input through the pipe; it is shorthand for `2>&1 |`. This implicit redirection of the standard error to the standard output is performed after any redirections specified by the command.

The reserved word `time` causes timing statistics to be printed for the pipeline once it finishes. The statistics currently consist of elapsed (wall-clock) time and user and system time consumed by the command’s execution. The -p option changes the output format to that specified by POSIX. When the shell is in POSIX mode, it does not recognize `time` as a reserved word if the next token begins with a ‘-’. The `TIMEFORMAT` variable may be set to a format string that specifies how the timing information should be displayed. The use of `time` as a reserved word permits the timing of shell builtins, shell functions, and pipelines. An external time command cannot `time` these easily.

When the shell is in POSIX mode (see Bash POSIX Mode), `time` may be followed by a newline. In this case, the shell displays the total user and system `time` consumed by the shell and its children. The `TIMEFORMAT` variable may be used to specify the format of the time information.

If the pipeline is not executed asynchronously, the shell waits for all commands in the pipeline to complete.

Each command in a pipeline is executed in its own subshell. The exit status of a pipeline is the exit status of the last command in the pipeline, unless the `pipefail` option is enabled. If `pipefail` is enabled, the pipeline’s return status is the value of the last (rightmost) command to exit with a non-zero status, or zero if all commands exit successfully. If the reserved word ‘!’ precedes the pipeline, the exit status is the logical negation of the exit status as described above. The shell waits for all commands in the pipeline to terminate before returning a value.

Of course my software doens't contain pipelines. The more you know!


This software takes advantage of the simple commands to make a more simpler life!
