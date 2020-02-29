dnf install mariadb mariadb-server


dnf search php | grep "mbstring\|mysql\|xml\|zip"
dnf search php | grep "mbstring\|mysql"

dnf -y install php-curl
dnf search php | grep "mbstring"
dnf search php | grep "intl"
dnf search php | grep "gd"
dnf search php | grep "curl"
dnf search php | grep "imagick\|curl"
dnf search php | grep "imagick"
dnf search php

mkdir nextCloud
cd nextCloud/
curl -O https://download.nextcloud.com/server/releases/nextcloud-16.0.4.tar.bz2
tar xf nextcloud-16.0.4.tar.bz2

