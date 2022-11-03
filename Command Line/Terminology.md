## command

A command in the terminal is a program. By typing that command we execute that program. A command may take one or more arguments, but there are also command that don't need arguments

## argument

An argument is a piece of information that we pass in to a command, to influence it's behaviour.

## stdout - Standard Output

`stdout` is the standard output channel of the terminal. It creates one ore more lines without prepedning the prompt

## Prompt

The prompt provides us a give set of information, usually you'll see your username and the directory you're currently in. 

## mnt

`mnt` is the directory that includes all partitions of your hard drive(s).

## sudo - Super User Do

Sometimes commands need extra permissions to be executed. If our user doesn't have those permissions (and we are extremely sure that we wanna do it), we can use `sudo` to execute that command with elevated permissions. `sudo` will prompt you for your password and after you put it in it will execute.
If you want to redo your last command with `sudo` privileges, you can type `sudo !!`