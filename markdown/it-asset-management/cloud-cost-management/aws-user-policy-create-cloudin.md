---
title: Create an AWS IAM user policy for Cloud Cost Management
description: Create an Identity and Access Management \(IAM\) user profile that enables access to AWS data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/cloud-cost-management/aws-user-policy-create-cloudin.html
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Cloud Cost Management for AWS, Configure, Cloud Cost Management, IT Asset Management, Asset Management]
---

# Create an AWS IAM user policy for Cloud Cost Management

Create an Identity and Access Management \(IAM\) user profile that enables access to AWS data.

## Before you begin

You must know how to create an IAM user and set up a user policy. See the [AWS documentation on IAM](http://docs.aws.amazon.com) for details.

Use an auto-generated access key. You need the key information when you configure AWS credentials in the instance.

Roles required:

On the AWS Management Console: AWS Management Console administrator.

Cloud Cost Management: insights\_admin \[sn\_clin\_core.insights\_admin\] or admin.

## About this task

The following procedure describes the process of creating an AWS IAM user policy and configuring credentials-based authentication for Cloud Cost Management. If you prefer to use Assume Role authentication, see .

## Procedure

1.  Log in to the AWS Management Console and create a user in IAM.

2.  Save the Access Key ID and Secret Access Key.

3.  Attach permissions to the IAM user using either of the following methods:

    -   Grant administrator access to the user by attaching the Administrator Access policy.
    -   Create an IAM policy with a descriptive name and use the following JSON for billing, cloud watch, forecast, and actions.

<table id="table_p3c_lhv_njc"><thead><tr><th>

Operation

</th><th>

Policy

</th></tr></thead><tbody><tr><td>

Billing

</td><td>

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": [
                "s3:GetObjectVersion",
                "s3:GetObjectTorrent",
                "s3:GetObject",
                "s3:ListBucket",
                "s3:GetObjectTagging",
                "s3:ListMultipartUploadParts",
                "s3:ListBucketMultipartUploads",
                "s3:GetObjectVersion"
            ],
            "Resource": [
                "arn:aws:s3:::<S3BucketName>/*",
                "arn:aws:s3:*:<AWS Master Account ID>:job/*",
                "arn:aws:s3:::<S3BucketName>"
            ]
        },
        {
            "Sid": "VisualEditor1",
            "Effect": "Allow",
            "Action": [
                "s3:GetAccountPublicAccessBlock",
                "s3:ListAllMyBuckets",
                "s3:ListJobs"
            ],
            "Resource": "*"
        }
    ]
}
```

</td></tr><tr><td>

Cloud watch

</td><td>

```
{
   "Version": "2012-10-17",
   "Statement": [
       {
           "Sid": "VisualEditor0",
           "Effect": "Allow",
           "Action": [
               "cloudwatch:GetMetricData",
               "cloudwatch:ListMetrics"
           ],
           "Resource": "*"
       }
   ]
}

```

</td></tr><tr><td>

Describe Report Definitions

</td><td>

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": "cur:DescribeReportDefinitions",
            "Resource": "<BillingReportName>"
        }
    ]
}
```

</td></tr><tr><td>

Actions

</td><td>

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": [
                "ec2:DescribeInstances",
                "ec2:StartInstances",
                "ec2:ModifyInstanceAttribute",
                "ec2:StopInstances",
                "ec2:DescribeInstanceStatus"
            ],
            "Resource": "*"
        }
    ]
}

```

</td></tr><tr><td>

AWS Cost Explorer, Forecast, and Reservation Purchase Recommendation APIs for the IAM user that you configure to access billing data on the Service account

</td><td>

```
{
   "Version": "2012-10-17",
   "Statement": [
       {
           "Sid": "VisualEditor0",
           "Effect": "Allow",
           "Action": [
               "ce:GetCostAndUsage",
               "ce:GetCostForecast",
               "ce:GetReservationPurchaseRecommendation"
           ],
           "Resource": "*"
       }
   ]
}

```

</td></tr><tr><td>

AWS Auto-scale instances \(Auto-scale instances aren’t included in Business Hours recommendations\)

</td><td>

```
{
     "Version": "2012-10-17",
     "Statement": [{
           "Sid": "VisualEditor0",
           "Effect": "Allow",
           "Action": [
                "autoscaling:DescribeAutoScalingInstances",
                "autoscaling:DescribeAutoScalingGroups"
           ],
           "Resource": "*"
     }]
}
```

</td></tr><tr><td>

AWS trusted advisor roles

</td><td>

```
{

    "Version":"2012-10-17",		 	 	 
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "support:DescribeTrustedAdvisorCheckRefreshStatuses",
                "support:DescribeTrustedAdvisorCheckResult",
                "support:DescribeTrustedAdvisorChecks",
                "support:DescribeTrustedAdvisorCheckSummaries",
                "support:RefreshTrustedAdvisorCheck",
                "trustedadvisor:Describe*"
            ],
            "Resource": "*"
        }
    ]
}
```

</td></tr></tbody>
</table>
