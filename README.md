# AWS VPC Peering Project

## Project Overview
This project demonstrates private network connectivity between two Amazon Web Services (AWS) Virtual Private Clouds (VPCs) using VPC Peering.

The project was implemented in the AWS Mumbai Region (`ap-south-1`) to enable communication between resources in separate VPCs using private IP addresses.

## Objectives
- Create and configure two VPCs.
- Configure public and private subnets.
- Establish a VPC Peering connection.
- Configure route tables for communication between VPCs.
- Configure security groups to allow required ICMP traffic.
- Test connectivity between EC2 instances using private IP addresses.

## AWS Services Used
- Amazon VPC
- VPC Peering
- Amazon EC2
- Subnets and Route Tables
- Internet Gateway
- Security Groups

## Network Configuration

| Resource | Configuration |
|---|---|
| AWS Region | Mumbai (`ap-south-1`) |
| VPC A | `10.10.0.0/16` |
| VPC B | `10.20.0.0/16` |
| Public Subnet A | `10.10.1.0/24` |
| Private Subnet A | `10.10.2.0/24` |
| Private Subnet B | `10.20.1.0/24` |
| VPC Peering | Active |

## EC2 Instances
- **EWB-Bastion-A:** Public subnet in VPC A.
- **EWB-App-A:** Private subnet in VPC A.
- **EWB-App-B:** Private subnet in VPC B.

## Testing and Results
Connectivity was tested from the bastion EC2 instance using the `ping` command and private IP addresses.

- VPC A bastion to EWB-App-A (`10.10.2.39`): Successful.
- VPC A bastion to EWB-App-B (`10.20.1.221`): Successful.

These tests demonstrated connectivity within VPC A and across the VPC Peering connection.

## Project Deliverable
The editable project report is available in this repository.

## Key Learning Outcomes
- AWS VPC and subnet configuration.
- Route table management.
- VPC Peering setup.
- Security group configuration.
- Private IP connectivity testing.

## Author
Suraj Prajapati.
