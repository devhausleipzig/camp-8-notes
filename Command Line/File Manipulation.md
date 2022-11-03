## cp - Copy

`cp` takes two arguments, the first is the __source__ and the second one is the __target__. It creates a duplicate of the source and puts it on the file system with the target name.

## mv - Move

`mv` works similar to `cp`, but doesn't create a duplicate but moves the file (delete the old instance and create a new one). You can also use `mv` to rename a file oder directory.

## rm - Remove

`rm` takes one argument and deletes that file. If we want to remove a directory, we need to provide the *recursive* option `-r` (e.g. `rm -r directory`).  

## > - Redirect

It takes stdout and redirects it to a file.
`ls -al > file.txt` -> takes the output of `ls` and instead of printing it to `stdout`, we save the output to a file.If we use `>` we overwrite the current contents of the file.

## >> - Append

`>>` works similar to `>`, but doesn't overwrite the file. It will append the output to the *end* of the file.



