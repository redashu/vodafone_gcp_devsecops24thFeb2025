## Understanding Multi container image build and container create 

<img src="multi1.png">

### Installing docker compose on gcp vm 

```
on-vm:~$ sudo -i
root@common-vm:~#  curl -SL https://github.com/docker/compose/releases/download/v2.33.1/docker-compose-linux-x86_64 -o /usr/bin/docker-compose
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0
100 70.2M  100 70.2M    0     0  32.0M      0  0:00:02  0:00:02 --:--:-- 99.6M
root@common-vm:~# 
root@common-vm:~# 
root@common-vm:~# chmod  +x /usr/bin/docker-compose  
root@common-vm:~# docker-compose  version 
Docker Compose version v2.33.1
root@common-vm:~# 


```

### compose yaml file 

```yaml
services:
  ashu-python-app:
  # image we want to build 
    image: ashu-pyapp:samplev1
    # location and name of Dockerfile  
    build:
      context: ./pyapp
      dockerfile: Dockerfile  
  ashu-web-app:
    image: ashu-webapp:samplev1 
    build: . 
```
### to build 
```sh
docker-compose build 
```
