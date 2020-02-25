# Installation

Add the repository url

```bash
cat << EOF > /etc/yum.repos.d/unit.repo
[unit]
name=unit repo
baseurl=https://packages.nginx.org/unit/fedora/$releasever/$basearch/
gpgcheck=0
enabled=1
EOF
```

Install the basic package with no extension

```bash
# yum install unit
```

# Main's files

- (**Socket**) /var/run/unit/control.sock
- (**Bin**) /usr/sbin/unitd 
- (**Log file**) /var/log/unit/unit.log 
- (**Pid file**) /var/run/unit/unit.pid


# Query

The GET request on an empty server

```bash
$ curl -X GET --unix-socket /var/run/unit/control.sock  http://localhost
{
	"certificates": {},
	"config": {
		"listeners": {},
		"applications": {}
	}
}
```

Focus only on listener and applications

```bash
$ curl -X GET --unix-socket /var/run/unit/control.sock  http://localhost/config
{
	"listeners": {},
	"applications": {}
}
```

# Create a static web server

Create a config file, **conf.json** with the following content

```json
# config.json
{
	"listeners": {
		"172.104.248.140:80": {
			"pass": "routes"
		}
	},

	"routes": [
		{
			"action": {
				"share": "/www/data/static/"
			}
		}
	]
}
```

Update the micro-service with this content

```bash
curl -X PUT --data-binary @config.json --unix-socket /var/run/unit/control.sock  http://localhost/config
```

