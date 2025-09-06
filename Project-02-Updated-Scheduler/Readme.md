# Project 02 – Automated Scheduled EC2 Start/Stop with Email Notifications

This project extends **Project 01** by integrating **Amazon SNS** to send email notifications every time an EC2 start or stop action is triggered by the Lambda function.

## Contents
- `Automated Scheduled EC2 StartStop With Email Notifications.docx` – Detailed documentation of the project.

## Improvements Over Project 01
- Added **Amazon SNS** integration for email notifications.
- Implemented **least privilege IAM policies** instead of using AmazonEC2FullAccess or AmazonSNSFullAccess.


## How It Works
1. Create an SNS Topic and subscribe your email.
2. Update Lambda code to publish to SNS after each start/stop action.
3. Attach custom IAM policies:
   - `EC2StartStop` → allows only start/stop for the specific instance.
   - `SNSPublish` → allows publishing messages to the SNS topic.
4. Schedule with EventBridge rules to auto-trigger Lambda at fixed times.
5. Receive email notifications whenever the instance is started or stopped.

## Clean Up
To avoid ongoing costs after testing this project, make sure to:
- Delete the **EventBridge rules** that trigger the Lambda function.
- Delete the **Lambda function** if not needed anymore.
- Remove the **SNS topic and subscription** used for email notifications.
- Terminate or stop the **EC2 instance** if it’s no longer required.
- Detach or delete any custom **IAM policies/roles** created for this project.

Cleaning up ensures you don’t incur charges beyond the AWS Free Tier.

## Author
Project contribution by Akanksha under *aws projects* repository.