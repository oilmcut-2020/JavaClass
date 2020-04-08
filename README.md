# HOW TO INSTALL DOCKER ?

1)Open file install_docker.sh 

**OR**

2) Copy this :
```
#!/bin/bash

sudo apt-get update
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo apt-key fingerprint 0EBFCD88

sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"

sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io

sudo docker run hello-world

echo "docker installed !!!"

```
3) Open terminal 
4) Type : 

        nano docker.sh
Please refer below screenshot :             
<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/docker-eclipse/images/d1.png">
</p>

5) Copy the Code from install_docker.sh and paste in  nano docker.sh
Please refer below screenshot :  

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/docker-eclipse/images/d2.png">
</p>

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/docker-eclipse/images/d3.png">
</p>

6) Press **Ctrl+S** & **Ctrl+X**
Please refer below screenshot : 
<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/docker-eclipse/images/d4.png">
</p>

7) Type :

        sh docker.sh
Please refer below screenshot : 
<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/docker-eclipse/images/d5.png">
</p>

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/docker-eclipse/images/d6.png">
</p>

---------------------------------------------------------------------------------------------------------------------------

# HOW TO INSTALL ECLIPSE IN YOUR COMPUTER ?

