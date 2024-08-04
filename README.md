# Terragrunt and yaml based GCP Infra
![enter image description here](https://github.com/cloudon-one/gcp-terragrunt-lz/blob/main/hld.jpeg)
## Dependencies

- [GCP SDK](https://cloud.google.com/sdk/docs/install)
- [Terraform 1.5+](https://developer.hashicorp.com/terraform/downloads?product_intent=terraform)
- [Terragrunt 0.4+](https://terragrunt.gruntwork.io/docs/getting-started/install/)

## Required GCP Permissions to Deploy Landing Zone

- Billing Account User
- Organization Viewer
- Folder Admin
- Compute Storage Admin
- Project Creator
- Project IAM Admin
- Folder Admin
- XPN Admin

## Start

Authenticate with GCP SDK

    gcloud auth application-default login
    cd envs/global/admin
    terragrunt init
    terragrunt apply

