### Revision 

### Development to Deployment 

<img src="dev1.png">

### CodeBuild option there 

<img src="cb1.png">

### clone repo and change password 

```
earntechbyme@common-vm:~$ ls
ashu-vodafone-webapp  my-codes  vscode
learntechbyme@common-vm:~$ git clone git@github.com:redashu/ashu-vodafone-webapp.git^C
learntechbyme@common-vm:~$ 
learntechbyme@common-vm:~$ 
learntechbyme@common-vm:~$ sudo -i
root@common-vm:~# 
root@common-vm:~# passwd learntechbyme 
New password: 
Retype new password: 
passwd: password updated successfully
root@common-vm:~# 

```

### testing container app

```
docker run -itd --name ashuc1 -p 1234:80 ashu:app1
fbf41b5ae610e514473600887f181d1711d01849c7b6b6356c926605525a75dd
learntechbyme@common-vm:~/ashu-vodafone-webapp$ docker ps
CONTAINER ID   IMAGE       COMMAND              CREATED         STATUS         PORTS                                     NAMES
fbf41b5ae610   ashu:app1   "httpd-foreground"   3 seconds ago   Up 2 seconds   0.0.0.0:1234->80/tcp, [::]:1234->80/tcp   ashuc1
learntechbyme@common-vm:~/ashu-vodafone-webapp$ 


```

## webapp working / functional testing can be done using automation tools as well

<img src="tool1.png">

