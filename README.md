# Terraform Learning

## Semantic Versioning
This proj is going to utilize semantic versionf for its tagging.
[semver.org](https://semver.org/)

The general format :
**MAJOR.MINOR.PATCH**, eg. `1.0.1`:

- **MAJOR** version when you make incompatible API changes
- **MINOR** version when you add functionality in a backward compatible manner
- **PATCH** version when you make backward compatible bug fixes

- https://semver.org/

## Install Terraform CLI

### Instruction from terrafrom site
[Install Terraform CLI](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli)

### For gitlab 
[Gitpod Lifecycle](https://www.gitpod.io/docs/configure/workspaces/tasks)

### Linux script consideration to make it more portable.

`#!/usr/bin/env bash`  should be included in bash script

#### Linux permission for script should be :
`chmod u+x <script_name>`

eg. 
```sh
chmod u+x ./bin/install_terraform_cli.sh
```

##### Running script `./` shorthand methor
eg. `source ./bin/install_terraform_cli.sh`

OR

##### Running script from gitpod.yml we need to point to a program to interpret it. 

eg. `./bin/install_terraform_cli.sh`

## Project Env variable 
### using env files
Create .env file
eg. `touch .env.example`

Then create env variable in file
eg. `PROJECT_ROOT='/workspace/terraform-beginner-bootcamp-2023'`

### Using gp env command

gp env AWS_ACCESS_KEY_ID=''
gp env AWS_SECRET_ACCESS_KEY=''
gp env AWS_DEFAULT_REGION='us-east-1'


## AWS CLI Installation

AWS CLI is installed in this project

To check AWS credentials is configured properly
```sh
aws sts get-caller-identity
```
## Terrafrom Basic

### Terrafrom Registry

[registry.terraform.io](https://registry.terraform.io/)

- **Providers** is an interface to API that will allow to create resources in terraform
- **Modules** are a way to make large amount of terraform code modular , portable and shareable

### Terrform commands

`terraform init` : start of new project we run this command . It downloads the binaries for terraform providers that we will use in this project

`terraform plan` : This will generate out a changeset about the state of our infra and what will bw changed

`terraform apply` : This will run a plan and pass the changeset to provider api.
`terraform apply --auto-approve`

`terraform output` : This will show outputs of all the files
