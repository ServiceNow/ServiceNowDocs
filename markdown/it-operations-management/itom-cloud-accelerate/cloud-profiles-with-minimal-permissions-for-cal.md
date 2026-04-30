---
title: Cloud profiles with minimal permissions for Cloud Action Library actions and subflows
description: You need appropriate cloud permissions to execute the Cloud Action Library actions and subflows. Edit the cloud permissions profile JSON to suit the needs of your organization.
locale: en-US
release: yokohama
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Cloud Action Library reference, Cloud Action Library, ITOM Cloud Accelerate, IT Operations Management]
---

# Cloud profiles with minimal permissions for Cloud Action Library actions and subflows

You need appropriate cloud permissions to execute the Cloud Action Library actions and subflows. Edit the cloud permissions profile JSON to suit the needs of your organization.

## Amazon Web Services \(AWS\) profile with minimal permissions

```json
{
	"Version": "2012-10-17",
	"Statement": [{
		"Sid": "VisualEditor0",
		"Effect": "Allow",
		"Action": [
			"iam:GenerateCredentialReport",
			"s3:GetEncryptionConfiguration",
			"ec2:DescribeInstances",
			"s3:ListBucketVersions",
			"ec2:DescribeRegions",
			"s3:ListBucket",
			"iam:GetCredentialReport",
			"iam:DeleteLoginProfile",
			"ec2:MonitorInstances",
			"iam:GetLoginProfile",
			"ec2:DescribeImages",
			"s3:PutEncryptionConfiguration",
			"ec2:StopInstances",
			"s3:GetBucketAcl"
		],
		"Resource": "*"
	}]
}
```

## Microsoft Azure profile with minimal permissions

```json
{
	"properties": {
		"roleName": "CCGAzureMinimalPermission",
		"description": "Grants access to scan compute resources from the Azure subscription",
		"assignableScopes": [
			"/subscriptions/${subscription_id}"
		],
		"permissions": [{
			"actions": [
				"Microsoft.ResourceGraph/resources/read",
				"Microsoft.Compute/virtualMachines/instanceView/read",
				"Microsoft.Compute/virtualMachines/*/powerOff"
			],
			"notActions": [],
			"dataActions": [],
			"notDataActions": []
		}]
	}
}
```

**Parent Topic:**[Cloud Action Library reference](cloud-action-library-reference.md)

