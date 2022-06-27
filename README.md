
## install 

### EC2 

```shell

aws ec2 run-instances --image-id ami-02c3627b04781eada --count 1 --instance-type t2.micro --key-name dotuian_icloud_key --security-group-ids sg-0621b911ac5d47a8f --subnet-id subnet-0023f3cd675fcf7c5

```

### docker 

```shell

ssh -i ~/dotuian_icloud_key.pem ec2-user@<instance_ip_address>

sudo amazon-linux-extras install docker
sudo service docker start

sudo usermod -a -G docker ec2-user
sudo chown $USER /var/run/docker.sock


sudo chkconfig docker on
sudo yum install -y git

sudo reboot

```

> https://docs.aws.amazon.com/ja_jp/AmazonECS/latest/developerguide/docker-basics.html


### docker-compose 

```shell
sudo curl -L https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
docker-compose version
```

### vpn_server.config

```shell
docker cp 7c06dfd8f246:/usr/vpnserver/vpn_server.config ./vpn_server.config
```

### start and stop instacne 

```shell
aws ec2 start-instances --instance-ids <instacne_id>

aws ec2 stop-instances --instance-ids <instacne_id>

aws ec2 terminate-instances --instance-ids <instacne_id>
```

