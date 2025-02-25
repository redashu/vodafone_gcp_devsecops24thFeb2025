## What is a Service Account?

A Service Account in GCP is a special kind of Google account used by applications, services, and virtual machines (VMs) to authenticate and access Google Cloud resources securely.

Unlike user accounts, service accounts are not tied to a human user but are instead used by programs, workloads, or other automated processes.

### Key Features of Service Accounts

- **Used for authentication:** Enables secure communication between services in GCP.
- **No passwords:** Uses OAuth 2.0 tokens and private keys for authentication.
- **Can be assigned IAM roles:** Service accounts can have permissions just like users.
- **Used by VMs, Cloud Functions, and APIs:** Allows services to access other Google Cloud resources securely.

### When to Use a Service Account?

| Use Case                       | Example                                                              |
|--------------------------------|----------------------------------------------------------------------|
| Running applications on VMs    | A web app running on Compute Engine accessing Cloud Storage         |
| Running scheduled jobs         | A Cloud Function that interacts with BigQuery                        |
| Automating infrastructure      | A Terraform script managing GCP resources                              |
| CI/CD pipelines                | A service account for deploying code to Cloud Run                      |

### Types of Service Accounts in GCP

| Service Account Type           | Description                                                        |
|--------------------------------|--------------------------------------------------------------------|
| User-Managed Service Accounts  | Created manually by users to authenticate workloads.               |
| Default Service Accounts       | Automatically created for Compute Engine, App Engine, Cloud Run, etc.|
| Google-Managed Service Accounts| Used internally by Google services (e.g., Cloud Storage, BigQuery).  |