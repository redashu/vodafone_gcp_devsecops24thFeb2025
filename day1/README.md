# vodafone_gcp_devsecops24thFeb2025

### Devops the Mindset

<img src="devops1.png">

### Devops to DevSecOps

<img src="devsecops1.png">

### Google cloud platform -- for Devops and Devsecops

<img src="ops1.png">

### Google Cloud account basic info 

<img src="info1.png">

### Web app use case 

<img src="web1.png">

## Observability in app 

### Metrics for Performance monitoring 

<img src="perm1.png">

### Few Gcp vm linux commands 

```sh
learntechbyme@gcp-common-vm:~$ whoami
learntechbyme
learntechbyme@gcp-common-vm:~$ ls /home
learntechbyme  somnathsalgar
learntechbyme@gcp-common-vm:~$ ls /home
learntechbyme  somnathsalgar
learntechbyme@gcp-common-vm:~$ ls /home
learntechbyme  pratikshasutar2032  somnathsalgar
learntechbyme@gcp-common-vm:~$ ls /home
ananthakumar_test  aniketkumbhar348921  learntechbyme  pradeepbhutare  pratikshasutar2032  shrishailraddi07  somnathsalgar
learntechbyme@gcp-common-vm:~$ who
learntechbyme pts/0        2025-02-24 07:24 (172.253.211.49)
somnathsalgar pts/1        2025-02-24 07:25 (172.253.211.49)
aniketkumbhar348921 pts/2        2025-02-24 07:25 (172.253.211.49)
pratikshasutar2032 pts/3        2025-02-24 07:26 (172.253.211.49)
ananthakumar_test pts/4        2025-02-24 07:26 (172.253.211.49)
shrishailraddi07 pts/5        2025-02-24 07:26 (172.253.211.49)
pradeepbhutare pts/6        2025-02-24 07:26 (172.253.211.49)
learntechbyme@gcp-common-vm:~$ 

```

### checking few details of cloudops agent 

```sh
learntechbyme@gcp-common-vm:~$ systemctl   status   google-cloud-ops-agent
● google-cloud-ops-agent.service - Google Cloud Ops Agent
     Loaded: loaded (/lib/systemd/system/google-cloud-ops-agent.service; enabled; preset: enabled)
     Active: active (exited) since Mon 2025-02-24 07:23:04 UTC; 5min ago
    Process: 1639 ExecStartPre=/opt/google-cloud-ops-agent/libexec/google_cloud_ops_agent_engine -in /etc/google-cloud-ops-agent/config.yaml (c>
    Process: 1687 ExecStart=/bin/true (code=exited, status=0/SUCCESS)
   Main PID: 1687 (code=exited, status=0/SUCCESS)
        CPU: 166ms

Feb 24 07:23:03 gcp-common-vm google_cloud_ops_agent_engine[1639]:   service:
Feb 24 07:23:03 gcp-common-vm google_cloud_ops_agent_engine[1639]:     pipelines:
Feb 24 07:23:03 gcp-common-vm google_cloud_ops_agent_engine[1639]:       default_pipeline:
Feb 24 07:23:03 gcp-common-vm google_cloud_ops_agent_engine[1639]:         receivers: [hostmetrics]
Feb 24 07:23:03 gcp-common-vm google_cloud_ops_agent_engine[1639]:         processors: [metrics_filter]
Feb 24 07:23:04 gcp-common-vm google_cloud_ops_agent_engine[1639]: 2025/02/24 07:23:04 [Ports Check] Result: PASS
Feb 24 07:23:04 gcp-common-vm google_cloud_ops_agent_engine[1639]: 2025/02/24 07:23:04 [Network Check] Result: PASS
Feb 24 07:23:04 gcp-common-vm google_cloud_ops_agent_engine[1639]: 2025/02/24 07:23:04 [API Check] Result: PASS
Feb 24 07:23:04 gcp-common-vm google_cloud_ops_agent_engine[1639]: 2025/02/24 07:23:04 Startup checks finished
Feb 24 07:23:04 gcp-common-vm systemd[1]: Finished google-cloud-ops-agent.service - Google Cloud Ops Agent.
learntechbyme@gcp-common-vm:~$ 
learntechbyme@gcp-common-vm:~$ 
learntechbyme@gcp-common-vm:~$ cd /opt/
learntechbyme@gcp-common-vm:/opt$ ls
google-cloud-ops-agent
learntechbyme@gcp-common-vm:/opt$ cd  google-cloud-ops-agent/
learntechbyme@gcp-common-vm:/opt/google-cloud-ops-agent$ ls
libexec  subagents
learntechbyme@gcp-common-vm:/opt/google-cloud-ops-agent$ 

```

### we can control ops agent  

```sh
 14  sudo systemctl   stop    google-cloud-ops-agent
   15  systemctl   status   google-cloud-ops-agent
   16  sudo systemctl   start    google-cloud-ops-agent
   17  systemctl   status   google-cloud-ops-agent
```
