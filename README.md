# Bash basics

Beginner in bash/shell-script? 

Below you find some help to commands that you will probaly need.

- [PWD](#pwd)
- [CD](#cd)
- [MKDIR](#mkdir)
- [LS](#ls)
- [TOUCH](#touch)

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



