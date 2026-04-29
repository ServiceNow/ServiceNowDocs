---
title: Configuring Service Control Policy in AWS
description: The AWS admin configures a Service Control Policy \(SCP\) and shares its ID with the ServiceNow AI Platform admin for Cloud Account Management setup. Cloud Account Management enforces the SCP via API calls to block resource creation in the account.
locale: en-US
release: australia
product: Cloud Account Management
classification: cloud-account-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up AWS cloud, Configuring cloud providers, Configuring Cloud Account Management, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Configuring Service Control Policy in AWS

The AWS admin configures a Service Control Policy \(SCP\) and shares its ID with the ServiceNow AI Platform admin for Cloud Account Management setup. Cloud Account Management enforces the SCP via API calls to block resource creation in the account.

The process involved in creating and using a Service Control Policy:

1.  The AWS admin sets up a Service Control Policy \(SCP\) in the management account, using a list of resources from the CFT script. The admin can customize this list by adding more resource types.
2.  The AWS admin shares the SCP ID with the ServiceNow admin, who uses it for registration during the Cloud Account Management configuration process.
3.  The Cloud Account Management app submits a suspension request, triggering an API call to the AWS Organizations Attach Policy API. This API enforces the SCP to block users from creating resources in that account.

Copy the following content to a file and save the file as CloudFormation template \(extension as \*.cft\):

```
AWSTemplateFormatVersion: 2010-09-09
Description: SCP policy for ServiceNow Cloud Workspace to restrict creation of new resources. 
Resources:
  PolicyTestTemplate:
    Type: AWS::Organizations::Policy
    Properties:
      Type: SERVICE_CONTROL_POLICY
      Name: CAM_SCP_SuspendAccount_Policy
      Content:
        Version: 2012-10-17
        Statement:
          - Sid: CAMSCPSuspendAccountPolicy
            Effect: Deny
            Action:
              - 'ec2:RunInstances'
              - 'ec2:CreateVolume'
              - 'ec2:CreateSnapshot'
              - 'ec2:CreateImage'
              - 's3:CreateBucket'
              - 'iam:CreateUser'
              - 'iam:CreateRole'
              - 'iam:CreatePolicy'
              - 'dynamodb:CreateTable'
              - 'sqs:CreateQueue'
              - 'sns:CreateTopic'
              - 'lambda:CreateFunction'
              - 'ec2:CreateVpc'
              - 'ec2:CreateSubnet'
              - 'ec2:CreateInternetGateway'
              - 'ec2:CreateRoute'
              - 'rds:CreateDBInstance'
              - 'redshift:CreateCluster'
            Resource: '*'
```

