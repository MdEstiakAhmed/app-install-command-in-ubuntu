```
sudo apt update
```

```
sudo apt-get install apt-transport-https ca-certificates curl gnupg lsb-release software-properties-common
```

```
sudo mkdir -p /etc/apt/keyrings
```

```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```
  
```
echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
  
```
sudo apt-get update
```

```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
```

```
sudo vi /etc/group
```
> add user to docker group

```exit
```

> from system logout and login

```
docker info
```

```
docker run hello-world
```

> show all container
```docker ps -a
```
