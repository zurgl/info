### How to use a remote server to see the web 

On the local machine, from a terminal :

```
$ ssh -D port user@serverName -qfN
```

**-D** : I have no idea 

**-q** : Be quiet 

**-f** : Putting background after logging 

**-N** : No idea too


You still have to configure the proxy for SOCK5 on firefox

localhost + port

### To keep the connection Alive

On the local machine edit **~.ssh/config**

```
Host *
  TCPKeepAlive yes
  ServerAliveInterval 120
```

On remote server edit **/etc/ssh/ssh_config** 

```
ClientAliveInterval 600
ClientAliveCountMax 0
```

Enjoy persistent ssh session 

More info - [link](https://askubuntu.com/questions/127369/how-to-prevent-write-failed-broken-pipe-on-ssh-connection)


### How to run a command

Just put the command after ssh call

```
$ ssh user@domain killall vim
```


### How to start ssh connexion for another port

Use -p option

```
$ ssh -p 1234 user@domain killall vim
```




