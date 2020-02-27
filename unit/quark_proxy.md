## Install quark

quick and easy

```
$ git clone https://git.suckless.org/quark
$ cd quark
$ make && make install
```
## Start quark 

Cannot be launch as root

```
$ sudo quark -h 127.0.0.1 -p 7878 -u user -g group -d /dir/ > quark.log &
```

## Configure unit

```
cat EOF < > config.json
{
  "listeners": {
    "xx.xx.xx.xx:pp" : {
      "pass":"routes"
    },
  
    "routes" : [
      {
        "action" : {
          "proxy": "http:"http://127.0.0.1:7878"
         }
       }
    ]
}

}
```
And its work you can serve video easy

