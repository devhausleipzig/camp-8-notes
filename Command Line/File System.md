```
home (dir)
| --- file1.txt
| --- file2.txt
| --- foo (dir)
	  | --- file3.txt
	  | --- file3.txt
	  | --- bar (dir)
		    | --- file4.txt
```

[[Terminology]]

## ls - List directory contents

The `ls` command is used to print out the current contents of the folder we are in. `ls` can work without an argument, but i can also take one. We have two types of arguments that we can pass in, that heavily change the behaviour.

### Folder as an argument

If we pass in a folder as the argument, `ls` print out the content of that folder

### Wildcard as an arguement

Example: `ls s*`
If we pass in a wildcard as the arguement, `ls` prints out all the __files__ that *match* our wildcard. We have three different types of wildcards.
- Starts with: `s*`
- Ends with: `*s`
- Includes: `*s*`

### Options (Flags)

We can change the way the output is presented to us, by passing different options. Options are passed by using the dash syntax `ls -option`. We can combine as many options as we like by just chaining them `ls -option1option2` (e.g. `ls -al`).

#### a - All files

Include directory entries whose names begin with a dot (‘.’).

#### l - Long format

List files in the long format, which means showing them in a list with additional information (e.g. owner, modified date).

## pwd - Print working directory

Outputs the __absolute__ path of the directory we are currently in.

## Absolute Path

Absolute paths are always constructed from the root of the file system (true for the context of the terminal).

## Relative Path

Relative paths are always constrcuted from the directory we are currently in.

## cd - Change directory

We us the `cd` command to navigate our file system. It takes exactly one argument. We can call it without an argument (syntactic sugar), but that just means the path to our home directory is filled in by the command.
The arugment that `cd` takes is a path, it can be absolute or relative.
If we want to go back one level we can use `cd ..`, which is the relative path to the parent directory.

## touch - Create files

`touch` takes one ore more arguments and creates a file for each argument passed. `touch file1.txt file2.txt` would create 2 files. We can also create files inside of __existing directories__ by prepending the filename with the directory.

## mkdir - Make directory

`mkdir` works similar to `touch`, but creates directories instead of files.


- 