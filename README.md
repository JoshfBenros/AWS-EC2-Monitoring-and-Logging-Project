# AWS-EC2-Monitoring-and-Logging-Project
This project demonstrates how to set up a secure and monitored AWS environment using a custom Virtual Private Cloud (VPC), EC2 instance, and CloudWatch/CloudTrail integrations. The configuration follows AWS best practices for cloud monitoring, logging, and network visibility.

# Project Overview

This project walks through the full setup of an EC2 instance in a custom VPC with monitoring, logging, and alerting features:

VPC Configuration – Created a custom VPC with CIDR block 10.0.0.0/16, subnet, route table, and internet gateway for public connectivity.

EC2 Instance Setup – Deployed a t3.micro instance in the public subnet running Amazon Linux 2023 with Apache (httpd) web server installed.

IAM Role Configuration – Created and attached the jb-ec2-cloudwatch-agent-role with the CloudWatchAgentServerPolicy for monitoring permissions.

CloudWatch Agent Installation – Installed and configured the CloudWatch agent on the EC2 instance to collect system metrics (CPU, memory, disk, network).

CloudWatch Metrics & Alarms – Created alarms to track CPU usage (cpu_usage_user > 70%) and verify instance performance.

VPC Flow Logs – Captured inbound and outbound network traffic and sent the logs to a CloudWatch log group (/vpc/flowlogs/jb-monitoring-vpc).

CloudTrail Setup – Configured AWS CloudTrail for governance, auditing, and tracking of API activity across the AWS account.

S3 Log Storage – CloudTrail logs are delivered to a dedicated S3 bucket for long-term retention and auditing.
