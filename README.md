## 🔧 Input Variables

All variables have default values, so they are optional unless you want to override them.

| Name             | Description                         | Type           | Default                          | Required |
|------------------|-------------------------------------|----------------|----------------------------------|----------|
| `vpc_name`       | Name tag for the VPC                | `string`       | `"my-vpc"`                       | ❌       |
| `vpc_cidr`       | CIDR block for the VPC              | `string`       | `"10.0.0.0/16"`                  | ❌       |
| `azs`            | List of availability zones          | `list(string)` | `["us-east-1a", "us-east-1b"]`   | ❌       |
| `public_subnets` | List of public subnet CIDRs         | `list(string)` | `["10.0.1.0/24", "10.0.2.0/24"]` | ❌       |

> 💡 **Note:** Although these variables are not required due to default values, you can override them when using the module to customize your setup.
