# Terraform AWS VPC Module

This Terraform module creates an AWS VPC with public subnets and outputs the VPC ID.

---

## Requirements

| Name      | Version  |
|-----------|----------|
| terraform | >= 1.0.0 |
| aws       | >= 4.0   |

---

## Usage

```hcl
module "vpc" {
  source  = "julietwainoi/vpc/aws"
  version = "1.0.1"

  vpc_name       = "my-vpc"
  vpc_cidr       = "10.0.0.0/16"
  azs            = ["us-east-1a", "us-east-1b"]
  public_subnets = ["10.0.1.0/24", "10.0.2.0/24"]
}

```
## Inputs

| Name            | Description             | Type           | Default                          | Required |
|-----------------|-------------------------|----------------|----------------------------------|----------|
| vpc_name        | Name of the VPC         | `string`       | `"my-vpc"`                       | no       |
| vpc_cidr        | CIDR block for the VPC  | `string`       | `"10.0.0.0/16"`                  | no       |
| azs             | Availability Zones list | `list(string)` | `["us-east-1a", "us-east-1b"]`   | no       |
| public_subnets  | Public subnet CIDRs     | `list(string)` | `["10.0.1.0/24", "10.0.2.0/24"]` | no       |

## Outputs

| Name   | Description       |
|--------|-------------------|
| vpc_id | The ID of the VPC |


## License


MIT

