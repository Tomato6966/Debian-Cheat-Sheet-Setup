# How-to-setup-your-Linux-Server
How to setup your Linux Server and install nodejs, python, ffmpeg and java. Working good for Discord Bot hosting and other hostings!

## [**DISCORD SUPPORT SERVER INVITE**](https://support.milrato.eu)

## youtube tutorial:

[![](http://img.youtube.com/vi/mj0nKw3GQlc/0.jpg)](http://www.youtube.com/watch?v=mj0nKw3GQlc "Linux Tutorial")

# Console cmds
*Those commands are all needed to install and setup a Debian (Linux) Server for Bot hosting, and general stuff like everything!*

- [**Installing Essentials!**](#Installing-Essentials!)

- [**Installing nodejs v16 && npm v7.4**](#Installing-nodejs-v16-&&-npm-v7.4)

- [**Installing yarn (optional)**](#Installing-yarn-(optional))

- [**Install python**](#Install-python)

> - [**Installing pip**](#Installing-pip)

> - [**Installing pip3**](#Installing-pip3)

> - [**Installing python3.9**](#Installing-any-other-Python-Version,-here-3.9.1-It-will-take-at-least-5-Minutes,-just-wait...)

- [**Install FFMPEG**](#Install-FFMPEG)

- [**Install Java 13**](#Install-Java-13)

- [**Install a Lighttpd Server with php**](#Install-a-Lighttpd-Server-with-php)


## Installing Essentials!
**1. Install sudo**
```
apt-get install sudo
sudo apt-get install build-essential libcairo2-dev libpango1.0-dev libjpeg-dev libgif-dev librsvg2-dev curl
```

## Installing nodejs v16 && npm v7.4
```
sudo apt update
sudo apt install -y build-essential curl
curl -sL https://deb.nodesource.com/setup_16.x | sudo -E bash -
sudo apt install -y nodejs
```

## Installing yarn (optional)
```
curl -sL https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt update
sudo apt install -y yarn
```


## Install python

### Installing pip
```
sudo apt-get install python-pip
```
### Installing-pip3
```
sudo apt-get install python3-pip
```

### Installing any other Python-Version, here 3.9.1 *It will take at least 5 Minutes, just wait...*
```
curl -O https://www.python.org/ftp/python/3.9.1/Python-3.9.1.tar.xz
tar -xf Python-3.9.1.tar.xz
cd Python-3.9.1
./configure --enable-optimizations
make -j 4
sudo make altinstall
python3.9 --version
```

## Install FFMPEG
```
sudo apt update
sudo apt install ffmpeg
ffmpeg -version
```


## Install Java 13
```
wget https://download.java.net/openjdk/jdk13/ri/openjdk-13+33_linux-x64_bin.tar.gz
sudo mkdir -p /usr/lib/jvm
sudo tar zxvf openjdk-13+33_linux-x64_bin.tar.gz -C /usr/lib/jvm
sudo update-alternatives --install "/usr/bin/java" "java" "/usr/lib/jvm/jdk-13/bin/java" 1
sudo update-alternatives --set java /usr/lib/jvm/jdk-13/bin/java
java -version
```

## Install a Lighttpd Server with php
```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install lighttpd
sudo systemctl start lighttpd
sudo systemctl enable lighttpd
sudo apt-get install mariadb-server mariadb-client -y
sudo mysql_secure_installation
```
```
Answer all the questions as shown below:
Change the root password? [Y/n] n
Remove anonymous users? [Y/n] Y
Disallow root login remotely? [Y/n] Y
Remove test database and access to it? [Y/n] Y
Reload privilege tables now? [Y/n] Y
```
```
sudo apt-get install php php-cgi php-fpm php-mysql -y
sudo nano /etc/php/7.3/fpm/php.ini
```
Change the following line: (ctrl + w search for it)
```
cgi.fix_pathinfo=1
```
```
sudo nano /etc/php/7.3/fpm/pool.d/www.conf
```
Find the following line:
```
listen = /run/php/php7.3-fpm.sock
```
And replace it with the following line:
```
listen = 127.0.0.1:9000
```
```
sudo systemctl restart php7.3-fpm
```
```
sudo nano /etc/lighttpd/conf-available/15-fastcgi-php.conf
```
Find the following line:s
```
"bin-path" => "/usr/bin/php-cgi",
"socket" => "/var/run/lighttpd/php.socket",
```
And replace it with the following lines:
```
"host" => "127.0.0.1",
"port" => "9000",
```
```
sudo lighty-enable-mod fastcgi
sudo lighty-enable-mod fastcgi-php
```
```
sudo nano /etc/lighttpd/conf-available/example.com.conf
```
Add the following lines:
```
$HTTP["host"] == "www.example.com" {
    server.document-root = "/var/www/html/"
    server.errorlog      = "/var/log/lighttpd/example.com-error.log"
}
```
Save and close the file when you are finished. Then, enable the Virtual host with the following command:
```
ln -s /etc/lighttpd/conf-available/example.com.conf /etc/lighttpd/conf-enabled/
```
Now feel free to code your php website!
```
sudo nano /var/www/html/index.php
```
Example Content:
```
<?php phpinfo(); ?>
```
Save and close the file. Then, change the ownership of the Lighttpd document root directory to www-data with the following command:
```
chown -R www-data:www-data /var/www/html/
```
Finally, restart Lighttpd service to apply all the configuration changes:
```
systemctl restart lighttpd
```

# SUPPORT ME AND MILRATO DEVELOPMENT

You can always Support me by inviting one of my **own Discord Bots**

[![2021's best Music Bot | Lava Music](https://cdn.discordapp.com/attachments/748533465972080670/817088638780440579/test3.png)](https://lava.milrato.eu)
[![Musicium Music Bot](https://cdn.discordapp.com/attachments/742446682381221938/770055673965707264/test1.png)](https://dc.musicium.eu)
[![Milrato Multi Bot](https://cdn.discordapp.com/attachments/742446682381221938/770056826724679680/test1.png)](https://dc.milrato.eu)

## Sponsors

### BEST HOSTING | Bittmax.de
BITTMAX Quality is their solution.
Bittmax is our first and probably most important sponsor!

**What they are offering:**
> Quality LXC & KVM (Root) Server
> Minecraft Hosting, as well as BungeeCord Network Hosting support
> Cheap and fast Domains
> WEBHOSTING
> DISCORD, TEAMSPEAK, Setups / Music Bots
> GAME SERVER, Rust, Gary's Mod, ..

**Discord Server:**
[https://discord.gg/GgjJZCyYKD](https://discord.gg/GgjJZCyYKD)

**Website:**
[https://bittmax.de/](https://bittmax.de/])

GET **5%** OFF EVERYTHING FOR EVER!
Code: **`x10`**

### MC-Host24.de
MC-Host24.de is selling the Best Digital Hosting Services ever!
Like For games..

**What they are offering:**
> Quality LXC & KVM (Root) Server
> WORLDS BEST Minecraft Hosting,
> Cheap and fast Domains
> WEBHOSTING
> DISCORD, TEAMSPEAK, Setups / Music Bots
> GAME SERVER, Rust, Gary's Mod, ..

**Discord Server:**
[https://discord.com/invite/4dGuGXK4A4](https://discord.com/invite/4dGuGXK4A4)

**Website:**
[mc-host24.de](https://mc-host24.de/user/affiliate/3121])
