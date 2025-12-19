This is a simple notes app built with React and Django deployed using docker on AWS.

## Requirements

    -- AWS EC2 ubuntu Instance
    
    -- t2.micro
    
    -- minimum storage of 10GB
    
    -- set up a key pair
    
    -- give all permissions of network 


Install Docker

    sudo apt install docker.io -y

Verify:

    docker --version

Enable Docker on boot:

    sudo systemctl enable docker
    sudo systemctl start docker

Allow Docker Without sudo

    sudo usermod -aG docker ubuntu && newgrp docker

Verify:

    docker ps

 Install Docker Compose

    sudo apt install docker-compose -y

Verify:

    docker-compose --version

## Installation
1. Clone the repository
```
git clone https://github.com/LondheShubham153/django-notes-app.git
```

2. Build the app
```
docker build -t notes-app .
```

3. Run the app
```
docker run -d -p 8000:8000 notes-app:latest
```

## Nginx

Install Nginx reverse proxy to make this application available

`sudo apt-get update`
`sudo apt install nginx`

