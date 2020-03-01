## Install and configure mariadb (mysql)

Install db and configure root user
```
dnf install mariadb mariadb-server
systemctl start mariadb
mysql_secure_installation
```
Enable the service for reboot
```
systemctl enable mariadb
```

Configure the firewall
```
firewall-cmd --permanent --add-port=3306/tcp
firewall-cmd --add-port=3306/tcp
```

Configure the bdd
```
# mysql -u root -p

    > CREATE DATABASE nextcloud;
    > CREATE USER 'nextuser'@'localhost' IDENTIFIED BY 'nextpass';
    > GRANT ALL PRIVILEGES ON nextcloud.* TO 'nextuser'@'localhost';
    > FLUSH PRIVILEGES;
```


### Install php 

Install php and requiered module
```
dnf -y install php php-curl php-xml php-intl php-mbstring \ 
  php-zip php-imagick php-gd php-pear-MDB2-Driver-mysqli php-json
```

### Install nextcloud 

```
curl -O https://download.nextcloud.com/server/releases/nextcloud-16.0.4.tar.bz2
tar xf nextcloud-16.0.4.tar.bz2
cd nextCloud/
./occ maintenance:install --database "mysql"  --database-name "nextcloud" \ 
    --database-user "zurgl" --database-pass "zurgl" \ 
    --admin-user "admin" --admin-pass "adminpass"
```
