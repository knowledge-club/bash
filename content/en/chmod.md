## CHMOD

Comes from _change modes_. It is used to change the access control of a file or folder in order to allow owner, users or everyone to _read/write/exec_ a file.

Permissions on unix-based systems are based on bitcounts. We have 3 bits, one for read, one for write and one for exec, making it `000` (or _read write exec_), if we set `001`, by summing the bits we'll have `1` (because `001=1`), if we want to set all permissions to a file we can simply set `111` (and by summing we have `7` because the binary sum of `111` is `7`).

On another part we have to set permissions for the users. The order is _owner_ _users in group_ _users not in group_, so we can have 3 sets of bits `000 000 000` which means `owner user guest`. So we can set permissions by concatenating sums of bits like `654`, this means: Owner can read-write (`110=6`), users can read and execute (`101=5`) and guests can only read (`100=4`).

```sh
# Sets the permission to owner can do anything, users can read and execute and guests only read the file "permissions.txt"
chmod 754 permissions.txt
```