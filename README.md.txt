# AWS API Gateway with API Key Authentication & Lambda Running Python Code

This project sets up an API Gateway with API key-based authentication that triggers a Lambda function. The Lambda function runs Python code to create a **VPC** with subnets, **S3** bucket, and other AWS resources.

## Overview

- **API Gateway**: Exposes HTTP routes (`POST /create-vpc` and `GET /vpc-info`) secured by an API key.
- **Lambda**: Executes Python scripts to create AWS resources like VPC and Subnets.
- **S3**: Stores the outputs from the Python execution.

### API Flow
1. **POST /create-vpc**: Runs Python code to create a VPC and subnets.
2. **GET /vpc-info**: Returns the VPC and subnet IDs from the last creation stored in S3.

## Setup Instructions

1. **Configure AWS CLI**.
2. **Deploy the infrastructure** by running:
   ```bash
   make deploy
