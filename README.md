# This Wiki Is ment to give you an overview how to setup a LINUX (DEBIAN) Server

> It covers many things, from python over nodejs to java and webservers and more!
> Working good for Discord Bot hosting and other hostings!

### [**DISCORD SUPPORT SERVER INVITE**](https://support.milrato.eu)

***

# __**Table of Contents**__

- ## [**Home**](https://github.com/Tomato6966/how-to-setup-your-linux-server/wiki)

***

- [**__1 All needed Console Commands__**](https://github.com/Tomato6966/how-to-setup-your-linux-server/wiki/1-All-needed-Console-Commands)
    - [1.1 Directory Navigation](https://github.com/Tomato6966/how-to-setup-your-linux-server/wiki/1.1-Directory-Navigation)
    - [1.2 System Information](https://github.com/Tomato6966/how-to-setup-your-linux-server/wiki/1.2-System-Information)
    - [1.3 Hardware Information](https://github.com/Tomato6966/how-to-setup-your-linux-server/wiki/1.3-Hardware-Information)
    - [1.4 File and Directory Cmds](https://github.com/Tomato6966/how-to-setup-your-linux-server/wiki/1.4-File-and-Directory-Commands)
    - [1.5 Process Management](https://github.com/Tomato6966/how-to-setup-your-linux-server/wiki/1.5-Process-Management)
    - [1.6 File Permissions](https://github.com/Tomato6966/how-to-setup-your-linux-server/wiki/1.6-File-Permissions)
    - [1.7 Networking](https://github.com/Tomato6966/how-to-setup-your-linux-server/wiki/1.7-Networking)
    - [1.8 Archives (Tar Files)](https://github.com/Tomato6966/how-to-setup-your-linux-server/wiki/1.8-Archives-(Tar-Files))
        - [1.8.1 Zips (and unzipping)](https://github.com/Tomato6966/Debian-Cheat-Sheet-Setup/wiki/1.8.1-Zips)
    - [1.9 Search](https://github.com/Tomato6966/how-to-setup-your-linux-server/wiki/1.9-Search)
    - [1.10 File Transfers](https://github.com/Tomato6966/how-to-setup-your-linux-server/wiki/1.10-File-Transfers)
    - [1.11 Disk Usage](https://github.com/Tomato6966/how-to-setup-your-linux-server/wiki/1.11-Disk-Usage)
    - [1.12 User Information and Management](https://github.com/Tomato6966/how-to-setup-your-linux-server/wiki/1.12-User-Information-and-Management)
    - [1.13 Speedtest](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/1.13-Speedtest)
    - [1.14 Clear Cache](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/1.14-Clear-Cache)
    - [1.15 Disable Sleeping Processes (Suspending)](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/1.15-Disable-Sleeping-Processes-(Suspending))
    - [1.16 Remove Welcome Message](https://github.com/Tomato6966/Debian-Cheat-Sheet-Setup/wiki/1.16-Remove-Welcome-Message)

***

- [**__2 Do that before everything__**](https://github.com/Tomato6966/how-to-setup-your-linux-server/wiki/2-Do-that-Before!)
    - [2.1 Youtube Tutorial](https://github.com/Tomato6966/how-to-setup-your-linux-server/wiki/2.1-Youtube-Tutorial)
    - [2.2 Installing Essentials](https://github.com/Tomato6966/how-to-setup-your-linux-server/wiki/2.2-Installing-Essentials)
    - [2.3 Insta Setup Linux Server](https://github.com/Tomato6966/how-to-setup-your-linux-server/wiki/2.3-Insta-Setup-Linux-Server)

***

- [**__3 Installing 3rd Party Packages__**](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/3-Install-3rd-Parties)
    - [3.0 All in One](https://github.com/Tomato6966/Debian-Cheat-Sheet-Setup/wiki/3.0-All-in-One)
    - [3.1 Nodejs & npm](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/3.1-Install-nodejs-and-npm)
    - [3.2 Yarn](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/3.2-Install-Yarn)
    - [3.3 Python](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/3.3-Install-python)
        - [*3.3.1 pip*](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/3.3.1-pip)
        - [*3.3.2 pip3*](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/3.3.2-pip3)
        - [*3.3.3 Python3.9*](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/3.3.3-python3.9)
        - [*3.3.4 Python3.10*](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/3.3.4-python3.10)
    - [3.4 FFMPEG](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/3.4-ffmpeg)
    - [3.5 Java](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/3.5-java)
        - [*3.5.1 Java 8*](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/3.5.1-java-8)
        - [*3.5.2 Java 11*](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/3.5.2-java-11)
        - [*3.5.3 Java 13*](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/3.5.3-java-13)
        - [*3.5.4 Java 15*](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/3.5.4-java-15)
        - [*3.5.5 Java 16*](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/3.5.5-java-16)
        - [*3.5.6 Java 17*](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/3.5.6-java-17)
        - [*3.5.7 Java 18*](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/3.5.7-java-18)
        - [*3.5.8 Java 18*](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/3.5.8-java-20)
        - [*3.5.9 Troubleshooting*](https://github.com/Tomato6966/Debian-Cheat-Sheet-Setup/wiki/3.5.8-Troubleshooting)
    - [3.6 Lighttpd with php](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/3.6-Lighttpd-with-php)
    - [3.7 Git](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/3.7-Git)
    - [3.8 Apache Webserver](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/3.8-apache-webserver)
        - [*3.8.1 MySQL*](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/3.8.1-mysql)
        - [*3.8.2 PHP*](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/3.8.2-php)
        - [*3.8.3 SSL Https*](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/3.8.3-ssl-https)
- [4 pm2 Tutorial](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/4-pm2-tutorial)
- [5 Mongodb (Database)](https://github.com/Tomato6966/Debian-Cheat-Sheet-Setup/wiki/5-Mongodb-Database)
- [6 lavalink Tutorial](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/6-lavalink-tutorial)
- [7 Linux Security](https://github.com/Tomato6966/Debian-Cheat-Sheet-Setup/wiki/7-Linux-Security)
    - [7.1 Firewall Security-Setup](https://github.com/Tomato6966/Debian-Cheat-Sheet-Setup/wiki/7.1-Firewall-Security-Setup)
    - [7.2 Tarpit False-Login loop](https://github.com/Tomato6966/Debian-Cheat-Sheet-Setup/wiki/7.2-Tarpit-False-Login-loop)
- [8 Support Me](https://github.com/Tomato6966/Debian-Cheat-Sheat-Setup/wiki/8-support-me)
