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