# How To Install Docker and Docker Compose on CentOS 7

### Step 1 — Install Docker

```
$ sudo yum check-update

$ curl -fsSL https://get.docker.com/ | sh

$ sudo systemctl start docker

$ sudo systemctl status docker

# Make sure it starts on every reboot
$ sudo systemctl enable docker
```

### Step 2 — Executing Docker Command Without Sudo (Optional)

```
$ sudo usermod -aG docker $(whoami)
```

OR

```
$ sudo usermod -aG docker username
```


### Step 3 - Install Docker Compose
```
$ sudo curl -L "https://github.com/docker/compose/releases/download/1.24.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

$ sudo chmod +x /usr/local/bin/docker-compose

$ docker-compose --version

```
