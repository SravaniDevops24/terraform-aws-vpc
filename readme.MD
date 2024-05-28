# custom AWS VPC Module

This module is developed for joindevops.com.  we are creating following resources. this module creates resources in  first 2 availability zones for  high availability HA

* vpc
* internet gateway
* internet gateway attaching to vpc
* 2 public subnets
* 2 private subnets
* 2 database subnets
* EIP
* NAT gate way 
* Public route tabel
* Private route table
* Database route table
* route table and subnet associations
* routes in all tables
* peering if required for user
* Routes in peering requestor and acceptor VPC
* Database subnet group

# inputs
* project_name (required): user should mention their projectt name.Type is string
* Environment (optional): default value is dev
* common_tags(Required): user should provide tags related to their project. Type is map
* vpc_cidr (optional): default value is 10.0.0.0/16. Type is string
* enable_dns_hostname (optional): defalut value is true. type is bool
* vpc_tags (optional): value is empty.type is map
* igw_tags(optional): value is empty.type is map
* public_subnet_cidrs(Required): user have to provide 2 valid subnet CIDR
* publis_subnet_cidr_tags (optional): default value is empty. type is map.
* private_subnet_cidrs(Required): user have to provide 2 valid subnet CIDR
* publis_subnet_cidr_tags (optional): default value is empty. type is map.
* database_subnet_cidrs(Required): user have to provide 2 valid subnet CIDR
* database_subnet_cidr_tags (optional): default value is empty. type is map.
* database_subnet_group_tags (optional): default value is empty. type is map.
* nat_gateway_tags (optional): default value is empty. type is map.
* public_route_table_tags (optional): default value is empty. type is map.
* private_route_table_tags (optional): default value is empty. type is map.
* database_route_table_tags (optional): default value is empty. type is map.
* is_peering_required (optional): Default value is false. type is bool.
* acceptor_vpc_id (optional): Default value is empty, default VPC id would be taken.type is string
* vpc_peering_tags (optional): Default value is empty. Type is map.

# outputs
* vpc_id: VPC ID
* public_subnet_ids: A list of 2 public subnet ids created 
* private_subnet_ids: A list of 2 private subnet ids created
* database_subnet_ids: A list of 2 database subnet ids created
* database_subnet_group_id: A databse subnet group id created
* igw_id: internet gateway id created 

