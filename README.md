# Terragrunt and yaml based GCP Infra

## Dependencies

- gcloud sdk
- terraform 1.3+
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
cd envs/global/admin
terragrunt init
terragrunt apply
```
Uncomment `remote_state` block within `global/terragrunt.hcl`
Init admin folder with remote state
```
cd envs/global/admin
terragrunt init
```
Type YES to confirm
