# AVO GCP

## Dependencies

- gcloud sdk
- terraform 1.0+
- terragrunt 0.35+

## Required permissions
-   Billing Account User
-   Organization Viewer
-   Folder Admin
-   Compute Storage Admin
-   Project Creator
-   Project IAM Admin
-   Folder Admin
-   Compute Shared VPC Admin

## Start

Authenticate with google sdk
```
gcloud auth application-default login
```
```
cd Environments/global/admin
terragrunt init
terragrunt apply
```
Uncomment `remote_state` block within `global/terragrunt.hcl`
Init admin folder with remote state
```
cd Environments/global/admin
terragrunt init
```
Type YES to confirm

In case of error: "bucket not found" run
 `terragrunt init --reconfigure`
```
ROOT FOLDER:
- mgmt-dev (eu)
 - host project:
    - vpc
    - vpn
    - dns
 - service project:
    - gke

- prod (us)
 - host project
    - vpc
    - vpn
    - dns
 - service project
    - gke
- global
- admin
    - iam
    - gcs

- dev (eu)
 - host project
    - vpc
    - vpn
 - service project
    - gke
    - sql
    - redis

- stg (eu)
 - host project
    - vpc
    - vpn
 - service project
    - gke
    - sql
    - redis

- stg (us)
   - host project
    - vpc
    - vpn
   - service project
    - gke
    - sql
    - redis  

- prod (eu)
 - host project
    - vpc
	  - vpn
 - service project
    - gke
    - sql
    - redis

- prod (us)
 - host project
    - vpc
    - vpn
 - service project
    - gke
    - sql
    - redis

- audit
 - audit
    - logs sink (pubsub)
