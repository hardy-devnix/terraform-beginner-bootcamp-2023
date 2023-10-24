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

eg. ```sh
chmod u+x ./bin/install_terraform_cli.sh
```

##### Running script `./` shorthand methor
eg. `source ./bin/install_terraform_cli.sh`

OR

##### Running script from gitpod.yml we need to point to a program to interpret it. 

eg. `./bin/install_terraform_cli.sh`

## Project Env variable 