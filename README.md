# simple-go-web-app-infra

## Description

This repo holds Terraform templates that provisions:
- A bastion server
- A new three-tier vpc
- Kubernetes suite on AWS (Control plane, Workder nodes, API load balancer). Note, this is a test Kubernetes setup that is with relatively simple architecture. Do not use for production. The other repo that provisions with cim / cloudformation is a better solution.

## How to run

```
cd aws/aws-account_one/network/vpc-simple-go-web-app
terraform init
terraform plan
terraform apply
```

```
cd aws/aws-account_one/bastion
terraform init
terraform plan
terraform apply
```

```
cd aws/aws-account_one/eks/cluster-simple-go-web-app
terraform init
terraform plan
terraform apply
```

## TODO
- Configure AWS S3 to store Terraform states
- Configure Dynamodb for locking

