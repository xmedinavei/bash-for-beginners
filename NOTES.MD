```
$ man [command]             # shows the manual of the command
$ whoami                    # shows the current user
$ tree                      # shows directory as a tree
$ pushd
$ popd
$ dirs -v
```


# List files
```
$ ls -a                     # list all files
$ ls S*                     # list all characters that start with S
$ ls [SC]*                  # list all files that start with S or C
$ ls *.md                   # list all .md extensions  
$ ls *.??                   # list all extensions that have 2 characters
$ ls [[:upper:]]*           # lsit any that starts with upper characters
```

# Find files
```
$ whereis bash                  # whereis locates the binary, source and manual files for the specified command names.
$ which bash                    # return the path of executable only
$ find . -name "*.md"           # finds the path of a expression in a directory
$ find /home -name file.txt     # find a file
$ find /home -iname file.txt    # no case sensitive
$ find . -type d                # find all directories
$ find . -type f                # find all files
```

# Files
```
$ mkdir -p dir1/dir2/dire3                          # create parents at the same time
$ touch dir1/text1.txt   
$ mv project01/text* project02/                     # move everything that matches 'text' into destination
$ cp project02/text1.txt project01/text1copy.txt
$ rm file*                                          # remove all that matches 'file'
$ rmdir project*                                    # remove all dires that matches 'project'
```

# View files
```
$ cat [file]                                    # see file
$ cat [file1] [file2]                           # see file both files
$ head -n 5 fakelog001.txt
$ tail -n 5 fakelog001.txt
$ more fakelog001.txt
$ less fakelog001.txt                           # navigate like man
$ grep [pattern] [file]
$ grep "174.212.2.233" fake002.log
$ grep "DELETE" fake002.log
```
# Variables
```
$ env                               # all env variables
$ echo $PATH                        # show the variable
$ export newvar=value               # create a new env var only in current session
```

# Redirection
```
$ env | grep "newVar" > output.txt                  # > saves the output into a file
$ env | grep "newVar" >> output.txt                 # >> appends
$ ls ./nodir 2> error.txt                           # 2 appends the error, if not '2' it doesnt write anything
$ ls ./nodir > error.txt 2>&1                       # 2>&1: This is another form of redirection. 2 represents the standard 
                                                    # error (stderr), and 1 represents the standard output (stdout). 
$ ls >> error.txt 2>&1                              # redirect standard output and error to te same file appending them
$ ls &>> error.txt                                  # redirect standard output and error to te same file appending them
```

# pipeline
```
$ ls -l /usr/bin | less
$ ls -l /usr/bin | grep echo
```

# persmissions
```
$ sudo chown root newFile.txt                       # change user
$ sudo chown :root newFile.txt                      # change group
$ chgrp vscode newFile.txt                          # change group
$ chmod 777 ./script.sh                             # give all permissions for owner group and user
```