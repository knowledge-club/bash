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

```sh
# Renames file "file.txt" to "file with spaces.txt"
mv file.txt file\ with\ spaces.txt
```
