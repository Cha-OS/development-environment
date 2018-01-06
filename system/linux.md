# Linux Server Install

## Basics

### Apps

```sh
apt-get install locate
updatedb
apt-get install zip
apt-get install joe
apt-get install usermode
apt-get install mc
apt-get install unzip
apt-get install htop
apt-get install screen
apt-get install lynx
apt-get install sysv-rc-conf
apt-get install perl
apt-get install rar
apt-get install unrar
```

Screen Usage

+ **http://www.pixelbeat.org/lkdb/screen.html**
+ `screen -d -r`
  + -d: disconnects from previous
  + -r: reconnect to the new one

### Config

```sh
joe /etc/hostname
> litterra.net
joe /etc/hosts
> 88.198.213.93 litterra.net
cat /etc/lsb-release
# DISTRIB_ID=Ubuntu
# DISTRIB_RELEASE=13.04
# DISTRIB_CODENAME=raring
# DISTRIB_DESCRIPTION="Ubuntu 13.04"
```

#### Setting locale

+ **https://people.debian.org/~schultmc/locales.html**

```sh
# list all available locales
locale -a
locale -a | grep en_ # list of available english locales
# list of supported
# en_US.UTF-8 UTF-8
cat /usr/share/i18n/SUPPORTED

/etc/locale.gen
# it was missing
# i have created it
touch /etc/locale.gen
/usr/sbin/locale-gen

apt-get update
apt-get install
dpkg-reconfigure locales

cat /etc/default/locale
	# LANG="en_US.UTF-8"
	# LANGUAGE="en_US:en"
joe ~/.pam_environment
> LANG="en_US.UTF-8"
> LANGUAGE="en_US:en"

apt-get install language-pack-en language-pack-en-base manpages
apt-get install --reinstall locales
joe /etc/skel/.bashrc
> # set locale
> export LC_ALL=en_US.UTF-8

# http://askubuntu.com/questions/162391/how-do-i-fix-my-locale-issue
sudo locale-gen "en_US.UTF-8"
sudo dpkg-reconfigure locales
```




cat /etc/default/locale
LANG="en_US.UTF-8"
LANGUAGE="en_US:en"
joe ~/.pam_environment
LANG="en_US.UTF-8"
LANGUAGE="en_US:en"
Configuring Locales
https://people.debian.org/~schultmc/locales.html
apt-get update
apt-get install
dpkg-reconfigure locales
apt-get install language-pack-en language-pack-en-base manpages
already installed
apt-get install --reinstall locales
export LC_ALL=en_US.UTF-8
set it in /etc/skel/.bashrc

# set locale
export LC_ALL=en_US.UTF-8
http://askubuntu.com/questions/162391/how-do-i-fix-my-locale-issue
sudo locale-gen "en_US.UTF-8"
sudo dpkg-reconfigure locales

# Mutual development

## Group access

### Disabling root login

+ http://www.howtogeek.com/howto/linux/security-tip-disable-root-ssh-login-on-linux/

```sh
joe /etc/ssh/sshd_config
> PermitRootLogin yes => PermitRootLogin no
# restarting the ssh deamon
service ssh restart
```

### Adding user

```sh
useradd -m mprinc -s /bin/bash
passwd mprinc
groupadd developers
usermod -a -G developers mprinc
```

### Setting up default file modes

+ http://www.linuxquestions.org/questions/linux-general-1/what-is-the-difference-between-chmod-and-setfacl-766617/
+ http://users.suse.com/~agruen/acl/linux-acls/online/

This didn't work

```sh
setfacl -d -m -R u::rwx /www
setfacl -d -m -R g::rwx /www
setfacl -d -m -R o::rx /www
```

### Group access to group folders

```sh
sudo mkdir /var/www/
# set the group owner
sudo chgrp developers -R .
# flag ‘s’ it will make all folders created underneath 
# to be owned by group developers
# only folders
# since xargs is optimizing invoking command 
# by grouping multiple lines into one command then
# -print0 is paired with -0 to deal properly with spaces and new lines
# http://man7.org/linux/man-pages/man1/xargs.1.html
sudo find . -type d -print0 | xargs -0 -L 10 sudo chmod g+srwx
# only files
sudo find . -type f -print0 | xargs -0 -L 10 sudo chmod g+rw
```

# Node

## Yarn

+ https://yarnpkg.com/en/docs/install#linux-tab