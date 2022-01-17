
## install 

### docker 

```shell
# sudo yum install docker

sudo amazon-linux-extras install docker
sudo service docker start
sudo usermod -a -G docker ec2-user

sudo chkconfig docker on
sudo yum install -y git

sudo reboot
```


### docker-compose 
```
sudo curl -L https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
docker-compose version
```



### vpn_server.config
```
docker cp 7c06dfd8f246:/usr/vpnserver/vpn_server.config ./vpn_server.config
```

