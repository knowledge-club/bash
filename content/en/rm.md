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