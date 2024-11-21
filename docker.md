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

> add user to docker group

```
sudo usermod -aG docker $USER
```

> from system logout and login

```
docker info
```

```
docker run hello-world
```

> if any permission issue occur then run
```
sudo chmod 666 /var/run/docker.sock
```

> show all container
```
docker ps -a
```


> docker service enable/disable while system boot (optional. ubuntu do it automatically)
```bash
sudo systemctl enable docker.service
sudo systemctl enable containerd.service

sudo systemctl disable docker.service
sudo systemctl disable containerd.service
```


### Docker desktop
```
https://docs.docker.com/desktop/setup/install/linux/ubuntu/
```
