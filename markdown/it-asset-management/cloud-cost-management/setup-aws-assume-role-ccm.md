---
title: Set up AWS Assume Role authentication for Cloud Cost Management
description: Configure AWS Identity and Access Management \(IAM\) roles and permissions to enable Cloud Cost Management using Assume Role authentication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/cloud-cost-management/setup-aws-assume-role-ccm.html
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-05-29"
reading_time_minutes: 4
breadcrumb: [Configure Cloud Cost Management for AWS, Configure, Cloud Cost Management, IT Asset Management, Asset Management]
---

# Set up AWS Assume Role authentication for Cloud Cost Management

Configure AWS Identity and Access Management \(IAM\) roles and permissions to enable Cloud Cost Management using Assume Role authentication.

## Before you begin

Make sure you meet the following requirements before configuring the Assume Role authentication:

Prerequisites on AWS side:

-   You have admin access to the AWS billing \(master\) account and all member accounts.
-   If your accounts already use the  **OrganizationAccountAccessRole**,  no additional role configuration is required.
-   If  the **OrganizationAccountAccessRole**  isn't present, you must create and attach the policies mentioned in the following procedure to the appropriate IAM roles in your  master or member accounts.

Prerequisites on Cloud Cost Management side:

The billing \(master\) account is configured without a Discovery credential. It should instead be configured with an Accessor account. For details, see the knowledge base article [KB0957891](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB0957891).

**Note:** If Discovery has already been configured using the  Assume Role  configuration, proceed without following the instructions in the knowledge article.

Roles required:

-   On the AWS Management Console: AWS Management Console administrator.
-   Cloud Cost Management: admin.

## About this task

When you configure AWS IAM roles and permissions using Assume Role authentication, the AWS Security Token Service \(STS\) issues temporary credentials. This enables cross-account access without long-lived credentials.

## Procedure

1.  Log in to the AWS Management Console for the master account.

2.  Navigate to **Identity and Access Management \(IAM\)** &gt; **Policies** &gt; **Create Policy**.

3.  Create an IAM policy with a descriptive name using either of the following methods:

    -   Create multiple individual policies and attach them all to the assume role.
    -   Create an inline policy that combines all the required statements and attach it to the assume role.
    You must replace `<S3BucketName>`, `<AWS Master Account ID>`, and `<BillingReportName>` with your actual values.

<table id="table_uqs_l2z_rjc"><thead><tr><th>

Operation

</th><th>

Policy

</th></tr></thead><tbody><tr><td>

Billing**Note:** This policy should be applied only on the master account.

</td><td>

Grants access to the S3 bucket that stores AWS billing reports. For example, `CCM-BillingS3Access`.

 ```
{ 
    "Version": "2012-10-17", 
    "Statement": [ 
        { 
            "Sid": "BillingS3Access", 
            "Effect": "Allow", 
            "Action": [ 
                "s3:GetObjectVersion", 
                "s3:GetObjectTorrent", 
                "s3:GetObject", 
                "s3:ListBucket", 
                "s3:GetObjectTagging", 
                "s3:ListMultipartUploadParts", 
                "s3:ListBucketMultipartUploads" 
            ], 
            "Resource": [ 
                "arn:aws:s3:::<S3BucketName>/*", 
                "arn:aws:s3:*:<AWS Master Account ID>:job/*", 
                "arn:aws:s3:::<S3BucketName>" 
            ] 
        }, 
        { 
            "Sid": "BillingAccess", 
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

Cloud watch**Note:** This policy should be applied both on the master and member account.

</td><td>

Enables retrieving Cloud watch metrics for cost and usage monitoring. For example, `CCM-CloudWatchAccess`.

 ```
{ 
   "Version": "2012-10-17", 
   "Statement": [ 
       { 
           "Sid": "CloudWatchMetricsAccess", 
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

Describe Report Definitions**Note:** This policy should be applied only on the master account.

</td><td>

Enables retrieving Cost and Usage Report \(CUR\) definitions. For example, `CCM-CURDefinitions`.

 ```
{ 
    "Version": "2012-10-17", 
    "Statement": [ 
        { 
            "Sid": "DescribeCURDefinitions", 
            "Effect": "Allow", 
            "Action": "cur:DescribeReportDefinitions", 
            "Resource": "<BillingReportName>" 
        } 
    ] 
} 
```

</td></tr><tr><td>

EC2 Actions**Note:** This policy should be applied both on the master and member account.

</td><td>

Enables viewing and managing EC2 instances for rightsizing and cost optimization. For example, `CCM-EC2Actions`.

 ```
{ 
    "Version": "2012-10-17", 
    "Statement": [ 
        { 
            "Sid": "EC2InstanceActions", 
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

AWS Cost Explorer, Forecast, and Recommendations**Note:** This policy should be applied both on the master and member account.

</td><td>

Grants access to  AWS Cost Explorer,  Cost Forecast, and  Reservation Purchase Recommendation  APIs. For example, `CCM-CostExplorerAccess`.

 ```
{ 
   "Version": "2012-10-17", 
   "Statement": [ 
       { 
           "Sid": "CostExplorerAccess", 
           "Effect": "Allow", 
           "Action": [ 
               "ce:GetCostAndUsage", 
               "ce:GetCostForecast" 
           ], 
           "Resource": "*" 
       } 
   ] 
} 
```

</td></tr><tr><td>

Auto Scaling**Note:**

-   Auto Scaling instances aren't included  in Business Hours recommendations.
-   This policy should be applied both on the master and member account.


</td><td>

Enables retrieving Auto Scaling instance details. For example, `CCM-AutoScalingAccess`.

 ```
{ 
     "Version": "2012-10-17", 
     "Statement": [
            { 
           "Sid": "AutoScalingDescribeAccess", 
           "Effect": "Allow", 
           "Action": [ 
                "autoscaling:DescribeAutoScalingInstances", 
                "autoscaling:DescribeAutoScalingGroups" 
           ], 
           "Resource": "*" 
            }
] 
} 
```

</td></tr><tr><td>

Trusted Advisor and Reservation Purchase Recommendation  APIs**Note:** This policy should be applied both on the master and member account.

</td><td>

Grants access to Trusted Advisor checks and Reservation Purchase Recommendations to support cost optimization insights. For example, `CCM-TrustedAdvisorAccess`.

 ```
{ 
    "Version":"2012-10-17",        
    "Statement": [ 
        { 
      "Sid": "RecommendationsAccess", 
            "Effect": "Allow", 
            "Action": [ 
                "support:DescribeTrustedAdvisorCheckRefreshStatuses", 
                "support:DescribeTrustedAdvisorCheckResult", 
                "support:DescribeTrustedAdvisorChecks", 
                "support:DescribeTrustedAdvisorCheckSummaries", 
                "support:RefreshTrustedAdvisorCheck", 
                "trustedadvisor:Describe*", 

          "ce:GetReservationPurchaseRecommendation" 
      ], 
            "Resource": "*" 
        } 
    ] 
} 
```

</td></tr></tbody>
</table>4.  Attach policies to the IAM role used for Assume Role authentication.

    1.  Navigate to **Identity and Access Management \(IAM\)** &gt; **Roles** and locate the role designated for Cloud Cost Management access.

        For example, **OrganizationAccountAccessRole**.

    2.  Select **Permissions** and then select **Attach policies**.

    3.  Search for and select the policy that you created in step 4.

    4.  Select **Add permissions** to confirm.

    \[Omitted image "aws-permission-policy.png"\] Alt text: AWS permission for IAM role in the AWS portal

5.  Grant permission to assume the role.

    1.  Navigate to **Roles** and open the **OrganizationAccountAccessRole** that you created in step 4.

    2.  Select the **Trust relationships** tab and then select **Edit trust policy**.

    3.  Verify that the principal is listed.

        For example, trust relationship on member account

        ```
        {
            "Version": "2012-10-17",
            "Statement": [
                {
                    "Effect": "Allow",
                    "Principal": {
                        "Service": "ec2.amazonaws.com"
                    },
                    "Action": "sts:AssumeRole"
                }
            ]
            }
        ```

        For example, trust relationship on master account

        ```
        {
            "Version": "2012-10-17",
            "Statement": [
                {
                    "Effect": "Allow",
                    "Principal": {
                        "AWS": "arn:aws:iam::<<member-account-number>>:role/<<assume-role-created-in-member-account>>"
                    },
                    "Action": "sts:AssumeRole",
                    "Condition": {}
                }
            ]
        }
        ```

    4.  Select **Update policy**.

    \[Omitted image "aws-trust-policy.png"\] Alt text: AWS trust policy in the AWS portal


## Result

After the policies are attached to the Assume Role, Cloud Cost Management can authenticate your AWS accounts using Assume Role and access billing, cost, and resource data.

