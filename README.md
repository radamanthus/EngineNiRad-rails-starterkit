# EngineNiRad Rails Starterkit

This is a collection of Terraform scripts to get you started with provisioning a Rails application on AWS using Terraform.

## Quick Start

Fork this repository then download.

```
git clone `https://github.com/yourawesomegithubusername/EngineNiRad-rails-starterkit.git`
cd EngineNiRad-rails-starterkit
```

Provision the global resources

```
cd global/s3
terraform init
terraform apply
```

Provision the admin-related resources

```
cd ../..
cd mgmt
cd vpc
terraform init
terraform apply
cd ..
cd services/bastion-host
terraform init
terraform apply
```

Provision the common resources for the staging environment

```
cd ../..
cd staging/vpc
terraform init
terraform apply
```

Provision the data storage resources

```
cd ..
cd services/data-storage/rds-postgresql
terraform-init
terraform apply
```

Provision the resources for the web layer

```
cd ../../..
cd services/web
terraform init
terraform apply
```
