# vodafone_gcp_devsecops24thFeb2025

### Service account in GCP 

<img src="svc1.png">

### Creating service account 

```sh
gcloud iam service-accounts create ashu-svc-new2  --project=vodafone-devsecops
```
### task 1

<img src="task1.png">

### Adding a predefine role to service account 

```sh
gcloud  projects  add-iam-policy-binding  vodafone-devsecops  --role="roles/compute.viewer" --member="serviceAccount:ashu-svc-new2@vodafone-devsecops.iam.gserviceaccount.com"
```

### creating custom role  and binding to service account 

```
 gcloud iam roles  create  ashuCustomRole  --project=vodafone-devsecops --title="comput engine roles permission" --permissions=compute.instances.create,compute.instances.delete,compute.instances.start  

 ====>>

gcloud  projects  add-iam-policy-binding  vodafone-devsecops  --role="projects/vodafone-devsecops/roles/ashuCustomRole" --member="serviceAccount:ashu-svc-new2@vodafone-devsecops.iam.gserviceaccount.com"
```