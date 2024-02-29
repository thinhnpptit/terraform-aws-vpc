## Terraform AWS VPC Module

### Usage
```hcl
module "vpc" {
  source  = "thinhnpptit/vpc/aws"
  version = "1.0.0"
  # insert the 3 required variables here
}
```
#### Required Inputs
These variables must be set in the module block when using this module.
- availability_zone list(string)
- private_subnet list(string)
- public_subnet list(string)
- vpc_cidr_block string (optional)
Default: "10.0.0.0/16"

### Resources
This is the list of resources that the module may create. The module can create zero or more of each of these resources depending on the count value. The count value is determined at runtime. The goal of this page is to present the types of resources that may be created.

This list contains all the resources this plus any submodules may create. When using this module, it may create fewer resources if you use a submodule.

This module defines 10 resources.

- aws_eip.nat
- aws_internet_gateway.ig
- aws_nat_gateway.public
- aws_route_table.private
- aws_route_table.public
- aws_route_table_association.public_association
- aws_route_table_association.public_private
- aws_subnet.private_subnet
- aws_subnet.public_subnet
- aws_vpc.vpc
