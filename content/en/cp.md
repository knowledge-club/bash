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

```sh
# Copy all files from ~/some_folder to ~/Documents/another_folder"
# You're in ~/some_folder
cp * ~/Documents/another_folder
```
