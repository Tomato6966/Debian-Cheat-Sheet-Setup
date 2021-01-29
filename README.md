# How-to-setup-your-Linux-Server
How to setup your linux server and install nodejs, python, ffmpeg and java. Working good for Discord Bot hosting and other hostings!

## youtube tutorial:

[![](http://img.youtube.com/vi/mj0nKw3GQlc/0.jpg)](http://www.youtube.com/watch?v=mj0nKw3GQlc "Linux Tutorial")

# Console cmds
*Those commands are all needed to install and setup a Debian (Linux) Server for Bot hosting, and general stuff like everything!*

## installing essentials!
**1. Install sudo**
- `$` ```apt-get install sudo```

**2. Install all needed dependences**
- `$` ```sudo apt-get install build-essential libcairo2-dev libpango1.0-dev libjpeg-dev libgif-dev librsvg2-dev```

## Installing nodejs v15 && npm v7.4
**1. Update all pkgs**
- `$` ```sudo apt update```

**2. Install Curl**
- `$` ```sudo apt install -y build-essential curl```

**3. Load the Nodejs source**
- `$` ```curl -sL https://deb.nodesource.com/setup_15.x | sudo -E bash -```

**4. Install nodejs globally**
- `$` ```sudo apt install -y nodejs```

## Installing yarn (optional)

**1. Load the YARN source**
- `$` ```curl -sL https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -```

**2. DOWNLOAD**
- `$` ```echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list```

**3. Update all pkgs**
- `$` ```sudo apt update```

**4. Install yarn globally**
- `$` ```sudo apt install -y yarn```


## Install python

### Installing 2.7.3

- `$` ```sudo apt-get install python-pip```

### Installing any version, here 3.9.1
**1. Get the Source**
- `$` ```curl -O https://www.python.org/ftp/python/3.9.1/Python-3.9.1.tar.xz```

**2. Extract the tar file**
- `$` ```tar -xf Python-3.9.1.tar.xz```

**3. Go to the new File**
- `$` ```cd Python-3.9.1```

**4. Configure the setup**
- `$` ```./configure --enable-optimizations```

**5. And create it**
- `$` ```make -j 4```

**6. Install python from the setup**
- `$` ```sudo make altinstall```

**7. Verify the Python installation**
- `$` ```python3.9 --version```

## Install FFMPEG

**1. Update all pkgs**
- `$` ```sudo apt update ```

**2. Install ffmpeg**
- `$` ```sudo apt install ffmpeg ```

**3. Verify the ffmpeg installation**
- `$` ```ffmpeg -version ```

## Installing Java (optional)
- `$` ```echo "deb http://ppa.launchpad.net/linuxuprising/java/ubuntu bionic main" | sudo tee/etc/apt/sources.list.d/linuxuprising-java.list```

- `$` ```sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 73C3DB2A```
- `$` ```sudo apt update```
- `$` ```sudo apt install oracle-java11-set-default```
- `$` ```sudo apt install openjdk-11-jdk```

### Manual installation of Java
- `$` ```curl -O https://download.java.net/java/GA/jdk11/9/GPL/openjdk-11.0.2_linux-x64_bin.tar.gz```
- `$` ```tar zxvf openjdk-11.0.2_linux-x64_bin.tar.gz```
- `$` ```sudo mv jdk-11* /usr/local/```
- `$` ```sudo vim /etc/profile.d/jdk.sh```
#### ADD:
- ```export JAVA_HOME=/usr/local/jdk-11.0.2 ```

   ```export PATH=$PATH:$JAVA_HOME/bin```
- `$` ```java -version```
