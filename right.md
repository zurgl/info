## Basic command about right

- cat /etc/group : List all group
- cat /etc/group : List all group
- id user : give user info (uid , gid ...)
- chown to change owner of file or directory
- chmod to change right to file or directory

```
drwxr-xr-x 2 zurgl zurgl 4096 Mar 31  2019 archive
drwxr-xr-x 4 zurgl zurgl 4096 Feb 24 17:49 deck
```

ten char, first one for the type, next user-group-all

- x : execure
- w : write
- r : read
- - : Nothing

Add read for user

```
$ chmod u+r . 
```

Remove write for groupe

```
$ chmod g-w . 
```

Add execute for other

```
$ chmod o+x . 
```

Remove execute for everyone

```
$ chmod a-x . 
```

## Octal

[https://doc.ubuntu-fr.org/permissions](for more)
