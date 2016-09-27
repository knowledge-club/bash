# Bash basics

Beginner in bash/shell-script? 

Below you find some help to commands that you will probaly need.

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
# **/** is a root of HD in unix systems (Linux, MacOS, ...). Similar to **c:** if yo're in a Windows.
cd /
```

Another example

```sh
# **~** is an alias to user's directory in unix systems. The complete path is anything like **/Users/darlanmendonca**
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
