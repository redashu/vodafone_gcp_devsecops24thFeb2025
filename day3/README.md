### Revision basic 

<img src="rev1.png">

### Container revision 

<img src="rev2.png">

### Container image build and run process

<img src="rev3.png">

### Network info 

<img src="rev4.png">

### Creating webapp container and access it as user 

### cloning sample code 

```
git  clone   https://github.com/schoolofdevops/html-sample-app.git
```

### Write dockerfile and build the image

```
learntechbyme@gcp-common-vm:~/my-codes$ ls
Dockerfile  html-sample-app
learntechbyme@gcp-common-vm:~/my-codes$ 
learntechbyme@gcp-common-vm:~/my-codes$ docker  build  -t  ashutoshh:apachev1  . 
2025/02/26 07:13:46 in: []string{}
2025/02/26 07:13:46 Parsed entitlements: []

```

### creating container and checking networking details 

```sh
docker  run -itd --name ashuweb  ashutoshh:apachev1 
b0433754345b959fc76623df1b409c93b70c1305c86b988d0aa4c14bac71dd1f
learntechbyme@gcp-common-vm:~/my-codes$ docker  ps
CONTAINER ID   IMAGE                COMMAND              CREATED          STATUS         PORTS     NAMES
b0433754345b   ashutoshh:apachev1   "httpd-foreground"   10 seconds ago   Up 9 seconds   80/tcp    ashuweb
learntechbyme@gcp-common-vm:~/my-codes$ 

```

### Recreating container with port mapping 

```
docker  rm  -f ashuweb  
ashuweb

learntechbyme@gcp-common-vm:~/my-codes$ docker  ps
CONTAINER ID   IMAGE                 COMMAND              CREATED              STATUS              PORTS     NAMES
c468918db995   sohail:apachev1       "httpd-foreground"   About a minute ago   Up About a minute   80/tcp    sohailweb
73802fd6be9e   somningshh:apachev1   "httpd-foreground"   6 minutes ago        Up 6 minutes        80/tcp    somningweb
30f7e834acea   aniketshh:apachev1    "httpd-foreground"   7 minutes ago        Up 7 minutes        80/tcp    aniketweb
0734d873089e   pradip:apachev1       "httpd-foreground"   7 minutes ago        Up 7 minutes        80/tcp    pradipweb
1d7948b120a1   anantha:httpd-v1      "httpd-foreground"   7 minutes ago        Up 7 minutes        80/tcp    Container-Anantha
b6e129e3d43a   anuj:apachev1         "httpd-foreground"   7 minutes ago        Up 7 minutes        80/tcp    anujweb


learntechbyme@gcp-common-vm:~/my-codes$ docker  run -itd --name ashuweb  -p  1234:80    ashutoshh:apachev1 
9d71f908ff2f7431acb176bbcdf248370555eda2e011235c7c7f4eba051320fc
learntechbyme@gcp-common-vm:~/my-codes$ docker  ps
CONTAINER ID   IMAGE                 COMMAND              CREATED          STATUS          PORTS                                     NAMES
9d71f908ff2f   ashutoshh:apachev1    "httpd-foreground"   3 seconds ago    Up 2 seconds    0.0.0.0:1234->80/tcp, [::]:1234->80/tcp   ashuweb
fb92de60dc59   anantha:httpd-v1      "httpd-foreground"   49 seconds ago   Up 48 seconds   0.0.0.0:8081->80/tcp, [::]:8081->80/tcp   AnanthaWeb2
c468918db995   sohail:apachev1       "httpd-foreground"   2 minutes ago    Up 2 minutes    80/tcp                                    sohailweb
73802fd6be9e   somningshh:apachev1   "httpd-foreground"   8 minutes ago    Up 8 minutes    80/tcp                                    somningweb
30f7e834acea   aniketshh:apachev1    "httpd-foreground"   8 minutes ago    Up 8 minutes    80/tcp       

```

### Updataing app code 

<img src="update.png">
