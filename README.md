# Bash basics

Beginner in bash/shell-script?

Below you find some help to commands that you will probaly need.

- [MAN](#man)
- [PWD](#pwd)
- [WHOAMI](#whoami)
- [PASSWD](#passwd)
- [DATE](#date)
- [CD](#cd)
- [LS](#ls)
- [MKDIR](#mkdir)
- [RMDIR](#rmdir)
- [CAT](#cat)
- [TAIL](#tail)
- [HEAD](#head)
- [TOUCH](#touch)
- [CP](#cp)
- [MV](#mv)
- [RM](#rm)
- [UNLINK](#unlink)
- [LN](#ln)
- [TRACEROUTE](#traceroute)
- [WHEREIS](#whereis)
- [WHICH](#which)
- [KILL](#kill)
- [SUDO](#sudo)
- [CHOWN](#chown)
- [CHMOD](#chmod)
- [FIND](#find)
- [ECHO](#echo)

## MAN

Shows the full description of a command.

```sh
# Shows help for `cat` command
man cat
```

## PWD

Show where you are in bash. The directory specifically. The command is an abbreviation to ***print working directory***.

```sh
pwd
```

will return a path like this

```sh
/Users/darlanmendonca/projects
```

## WHOAMI

The `whoami` command returns your username.

```sh
# Outputs your username
whoami
```

## PASSWD

The `passwd` command is used to change your password.

```sh
# You will be asked to type your current password and after this you have to type your new password twice
passwd
```

## DATE

The `date` command returns the current date and time

```sh
# Outputs current date and time
date
```

## CD

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

### Note

with space after command, you can pass multiples arguments to command. In case of ***cd*** command, you only need pass one arguments, but other commands maybe work with multiples. In cases of multiples arguments, just give a space between values.

## LS

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

### Note

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

## MKDIR

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

## RMDIR

Removes an empty directory.

```sh
# Removes newly created folder "fdr"
rmdir fdr
```

## CAT

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

## TAIL

Gets the ending content of a file and prints it out to the screen.

```sh
# Get the ending lines of error.log
tail error.log
```

There's also a possibility to read a stream of data in realtime, for instance, to read the apache error logs in real time while the server is executing.

```sh
tail -f apache/error.log
```

## HEAD

The oposite of `tail`, gets the first part of a file.

```sh
# Gets the first lines of error.log
head error.log
```

## TOUCH

This command is used to create files.

```sh
# create a file called index.html
touch index.html
```

```sh
# create files index.html, style.css and app.js in just one command
touch index.thml style.css app.js
```

## CP

Copies a file to another location.

```sh
# Copies the file "file.md" to the folder "files""
cp file.md /files/
```

Can also be used to create a copy of files in the `pwd` if you specify a __file__ name and not a __folder__ name.

```sh
# Creates a second file called "b.md" from "a.md"
cp a.md b.md
```

## MV

Moves or renames a file.

- If another directory is specified, then the file will be moved acording to the argument
- If the same directory is specified, but another filename, the file will be renamed

```sh
# Moving file "a.txt" to "/b" directory
mv a.txt /b/a.txt
```

```sh
# Renames file "a.txt" to "b.txt"
mv a.txt b.txt
```

## RM

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

## UNLINK

Removes a single file

```sh
# Deletes file "the_file.md"
unlink the_file.md
```

## LN

Creates links between files, can be seen as "shortcuts" of Windows users.

```sh
# Creates a "Shortcut" to file /bin/ls
ln -s ./list /bin/ls
```

## TRACEROUTE

Traces the internet route of a domain or IP (equivalent to `tracert` on Windows)

```sh
# Traces the route to domain.com
traceroute domain.com
```

## WHEREIS

Used to localize programs within the filesystem.

```sh
# Locate program php within the filesystem
whereis php
```

## WHICH

Same as _WHEREIS_ but locate programs inside the user's path.

```sh
# Locate program php within the users path
which php
```

## KILL

Send a signal to a process for it to finish or be killed.

```sh
# Kills process with ID 342
kill -9 342
```

## SUDO

Grants `root` privileges to the current command.

```sh
# Runs ls command as root
sudo ls
```

```sh
# Change the current user to root
sudo su
```

## CHOWN

Comes from _change owner_. It can change file/folder owners and groups.

```sh
# Changes the owner of the file called `file.md` to `wheel` and the group to `root`
chown wheel:group file.md
```

## CHMOD

Comes from _change modes_. It is used to change the access control of a file or folder in order to allow owner, users or everyone to _read/write/exec_ a file.

Permissions on unix-based systems are based on bitcounts. We have 3 bits, one for read, one for write and one for exec, making it `000` (or _read write exec_), if we set `001`, by summing the bits we'll have `1` (because `001=1`), if we want to set all permissions to a file we can simply set `111` (and by summing we have `7` because the binary sum of `111` is `7`).

On another part we have to set permissions for the users. The order is _owner_ _users in group_ _users not in group_, so we can have 3 sets of bits `000 000 000` which means `owner user guest`. So we can set permissions by concatenating sums of bits like `654`, this means: Owner can read-write (`110=6`), users can read and execute (`101=5`) and guests can only read (`100=4`).

```sh
# Sets the permission to owner can do anything, users can read and execute and guests only read the file "permissions.txt"
chmod 754 permissions.txt
```

## FIND

Searches a specific directory for a pattern.

```sh
# Finds the git directory recursively within a root folder
find . -name .git -type d
```

## ECHO

Prints out the arguments to standard output.

Echo is often used to pass on parameters to other commands' inputs, since it writes out to standard output, its output can be piped to another command's input stream.

```sh
# Prints "Hello" to the screen
echo "Hello"
```
