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

### K8s quick revision 

<img src="k8s1.png">

### getting credentails of GEK -- control plane 

<img src="k8s2.png">

### connection verification 

```
learntechbyme@cloudshell:~ (vodafone-devsecops)$ kubectl version 
Client Version: v1.29.13
Kustomize Version: v5.0.4-0.20230601165947-6ce0bf390ce3
Server Version: v1.29.13-gke.1169000
learntechbyme@cloudshell:~ (vodafone-devsecops)$ kubectl version  -o yaml 
clientVersion:
  buildDate: "2025-01-15T14:43:02Z"
  compiler: gc
  gitCommit: 9a58e9398d4aa69d7ad40f40407e54b96025e0c5
  gitTreeState: clean
  gitVersion: v1.29.13
  goVersion: go1.22.10
  major: "1"
  minor: "29"
  platform: linux/amd64
kustomizeVersion: v5.0.4-0.20230601165947-6ce0bf390ce3
serverVersion:
  buildDate: "2025-02-03T04:19:49Z"
  compiler: gc
  gitCommit: b4e8a905b211e97a81bbfe41602017d9a5bfef1c
  gitTreeState: clean
  gitVersion: v1.29.13-gke.1169000
  goVersion: go1.22.10 X:boringcrypto

```
