# Quick Web Server
Maybe you need a web server for a simple static site, Or test your server.

But it can be tedious to install, configure & fire up a web server on your local machine.

With this package, You can save some precious time & serve your static assets with this simple Docker Compose configuration.

## Installation
    git clone https://github.com/moghaddam24/QuickWebServer
    cd QuickWebServer
    
    docker-compose up -d


## Change Running port
If you want to change runnin port, You can open docker-compose.yml and change the this line.

    services:
    client:
        image: nginx
        ports:
            - 324:80 # Change 324 to any port which you want


## How to install docker on ubuntu 18 - 22

    sudo apt update

    sudo apt install apt-transport-https ca-certificates curl software-properties-common

    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

    echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

    sudo apt update
    apt-cache policy docker-ce
    sudo apt install docker-ce

You can check docker status with this command

    sudo systemctl status docker

## How to install docker compose
    
    sudo apt install docker-ce docker-ce-cli containerd.io docker-compose-plugin



## If you want to run docker as non-root user then you need to add it to the docker group.

Create the docker group if it does not exist

    $ sudo groupadd docker
        
Add your user to the docker group.

    $ sudo usermod -aG docker $USER
        
Log in to the new docker group (to avoid having to log out / log in again; but if not enough, try to reboot):

    $ newgrp docker
    
Check if docker can be run without root

    $ docker run hello-world
    
Reboot if still got error

    $ reboot
