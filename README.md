# AWS-VPC-Peering-Project
AWS VPC Peering with EC2 private connectivity

## Overview
This project demonstrates private communication between two Amazon Virtual Private Clouds (VPCs) using VPC Peering.

## Architecture

- **VPC A:** `10.10.0.0/16`
- **VPC B:** `10.20.0.0/16`
- **VPC A subnet:** Public and private subnets
- **VPC B subnet:** `10.20.1.0/24` (private)
- **VPC Peering:** `ewb-a-b-peer`
- **EC2 Instance A:** Amazon Linux 2023
- **EC2 Instance B:** Amazon Linux 2023

## Routing Configuration

- VPC A routes traffic for `10.20.0.0/16` through the peering connection.
- VPC B routes traffic for `10.10.0.0/16` through the peering connection.
- Existing local routes were retained.

## Security Configuration

- Security groups were configured to permit the required traffic.
- ICMP traffic from VPC A was allowed to test connectivity.

## Testing and Results

Connectivity was tested from EC2 Instance A to EC2 Instance B using:

```bash
ping 10.20.1.75
```

**Result:** 0% packet loss. Private communication between the two VPCs was successfully verified.

## Skills Demonstrated

- Amazon VPC
- IPv4 CIDR addressing and subnets
- Route tables and routing
- VPC Peering
- Amazon EC2
- Security groups
- Linux networking and connectivity testing

## Cleanup

Project resources should be terminated or deleted when no longer needed to avoid unnecessary AWS charges.



# Author Name : Jayendra Singh 

