# Bash basics

Beginner in bash/shell-script? 

Below you find some help to commands that you will probaly need.

- [PWD](#pwd)
- [CD](#cd)
- [MKDIR](#mkdir)
- [LS](#ls)
- [TOUCH](#touch)
- [RM](#rm)
- [WHEREIS](#whereis)
- [WHICH](#which)
- [CAT](#cat)
- [ECHO](#echo)
- [MAN](#man)
- [MV](#mv)
- [CP](#cp)
- [WC](#wc)
- [WHOAMI](#whoami)
- [PASSWD](#passwd)
- [DATE](#date)

### PWD
Show where you are in bash. The directory specifically. The command is an abbreviation to ***print working directory***.

```sh
pwd
```

will return a path like this

```sh
/Users/darlanmendonca/projects
```

### CD
Go to a path, relative or absolute. Is an abbreviation to ***change directory***

```sh
# '/'' is a root of HD in unix systems (Linux, MacOS, ...). Similar to 'c:' if yo're in a Windows.
cd /
```

Another example

```sh
# '~'' is an alias to user's directory in unix systems. The complete path is anything like '/Users/darlanmendonca'
cd ~
```

```sh
# path absolute
cd /Users/darlanmendonca
```

```sh
# relative path, I'm in /Users/darlanmendonca, and we want enter in directory projects, inside where we're.
cd projects
```

## Note
with space after command, you can pass multiples arguments to command. In case of ***cd*** command, you only need pass one arguments, but other commands maybe work with multiples. In cases of multiples arguments, just give a space between values.

### MKDIR
Command to ***make a directory***.

```sh
# create a directory called 'nomeDaPasta' in current path
mkdir nomeDaPasta
```

```sh
# create two or more directorys, just give space between arguments.
# in this case, we are create two directory, 'name1' and 'name2', both in the current path.
mkdir name1 name2
```

```sh
# create a directory called 'test' on path '/Users/darlanmendonca/Desktop'
mkdir /Users/darlanmendonca/Desktop/test
```

```sh
# -p is an flag(option), to create directories (in this case, directory 'parent'), case their not exists
mkdir -p /Users/darlanmendonca/Desktop/test/parent/children
```

### LS
Means ***list***. Useful to see what files exists in a path/current directory.

```sh
# I'm in '~', the command below list files in my current directory
ls
```

```sh
# list files in specific path
ls /Users
```

```sh
# If you want see hidden files, use the flag -a
ls -a /
```

```sh
# useful to check if a file exists, if file exists, return files founded, if not, return 'No such file or directory'
ls ~/Desktop/test.js
```

## Note
Always that you will write a path to a file, you can use glob files, to productivity. Glob files, is a way to set path to files using sets of filenames with wildcard characters.

```sh
# list only files in path, that have an extension .js
ls ~/Desktop/projeto1/*.js
```

```sh
# list only files in path, that have an extension .js
ls ~/Desktop/projeto1/*.js
```

```sh
# the double **, is to recursevely list inside projeto1
ls ~/Desktop/projeto1/**/*.js
```

### TOUCH
This command is used to create files.

```sh
# create a file called index.html
touch index.html
```

```sh
# create files index.html, style.css and app.js in just one command
touch index.thml style.css app.js
```

### RM
Means remove, is used to delete files or directories. <span color="red">**But be careful, this command dont send file to trash**</span>, they delete and dont have how undo.

```sh
# delete a file called index.html in current directory
rm index.html
```

```sh
# delete multiples files in a single command
rm index.html style.css
```

```sh
# finally to delete a directory, you need use flags r and f, respectively, both are abbreviation to recursive and force
rm -rf app
```

### WHEREIS

Used to localize programs within the filesystem.

```sh
# Locate program php within the filesystem
whereis php
```

### WHICH

Same as _WHEREIS_ but locate programs inside the user's path.

```sh
# Locate program php within the users path
which php
```

### CAT

Display contents of a file, or files.

`cat` will sequentially read and concatenate the contents of the input filenames and output them to stdout.

```sh
# Read and display contents of .gitignore file
cat .gitignore
```

```sh
# Read and displays the contents of multiple files
cat .gitignore .bowerrc .babelrc yourfile.css
```

### ECHO

Prints out the arguments to standard output.

Echo is often used to pass on parameters to other commands' inputs, since it writes out to standard output, its output can be piped to another command's input stream.

```sh
# Prints "Hello" to the screen
echo "Hello"
```

### MAN

Shows the full description of a command.

```sh
# Shows help for `cat` command
man cat
```

### MV

The `mv` command can be used to **move** or **rename** files.  

```sh
# Moves the foo.txt to bar folder
mv foo.txt bar/
```

```sh
# Renames the foo.txt to bar.txt
mv foo.txt bar.txt
```

### CP

The `cp` command is used to make copy of files and directories

```sh
# Creates a copy of foo.txt named bar.txt in the same folder you are in
cp foo.txt bar.txt
# If bar.txt already exists it will be overwritten without a confirmation
# If you want to confirm first you can use the -i flag
cp -i foo.txt bar.txt
```

```sh
# Creates a copy of foo.txt in bar folder
cp foo.txt bar/
```

```sh
# Creates a copy of foo.txt in bar folder with the name test.txt
cp foo.txt bar/test.txt
```

```sh
# Creates a copy of foo folder structure into bar folder
cp -R foo bar
```

### WC

The `wc` command returns the number of lines, words and characters there are in a file.

```sh
# Outputs the number of lines, words and characters in foo.txt file
# The output will be something like 2 3 18 foo.txt where:
# 2 is the number of lines, 3 is the number of words and 18 is the number of characters in the file
wc foo.txt
```

### WHOAMI

The `whoami` command returns your username.

```sh
# Outputs your username
whoami
```

### PASSWD

The `passwd` command is used to change your password.

```sh
# You will be asked to type your current password and after this you have to type your new password twice
passwd
```

### DATE

The `date` command returns the current date and time

```sh
# Outputs current date and time
date
```
