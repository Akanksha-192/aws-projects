# Project 01 – Automated Scheduled EC2 Start/Stop

This project demonstrates how to automate the start and stop of an Amazon EC2 instance on a defined schedule using AWS services like Lambda and EventBridge.  
It helps save costs by ensuring instances only run when needed.

## Contents
- `Automated Scheduled EC2 StartStop using AWS Lambda.docx` – Detailed documentation of the project.

## Tech Used
- **AWS Lambda** – Logic to start/stop EC2 instances.
- **EventBridge** – Cron rules for scheduling.
- **IAM Roles** – Permissions for automation.
- **EC2** – Target instance.

## How It Works
1. Create IAM Role with required permissions.
2. Deploy Lambda function with start/stop logic.
3. Configure EventBridge rules with cron expressions.
4. Verify automatic start/stop of instances.

## Author
Project contribution under *AWS Projects !!* repository.