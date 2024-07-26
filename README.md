# terraform-vpc-batch6

module "batch6" {
    
     
    source = ""
    version = "1.0.0"
    region = "us-east-2"
    vpc_cidr = "10.0.0.0/16"
    ip_on_launch =true
    port = [
        { from_port = 22,  to_port = 22 },
        { from_port = 80,  to_port = 82 },
        { from_port = 3306,  to_port = 3306 }
    ]

    subnet = [
        {  cidr  = "10.0.1.0/24", subnet_name = "kaizen1" },
        {  cidr  = "10.0.2.0/24", subnet_name = "kaizen2" },
        {  cidr  = "10.0.3.0/24", subnet_name = "kaizen3" }
        ]
        }