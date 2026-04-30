---
title: Prerequisites for executing scripts
description: Complete the prerequisites before you execute the AWS scripts.Set up an S3 bucket with read and delete privileges for the ServiceNow IAM role to store and delete the SendCommand API responses when importing AWS data.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 4
breadcrumb: [Configure the AWS environment, AWS, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Prerequisites for executing scripts

Complete the prerequisites before you execute the AWS scripts.

**Important:** Ensure that you have downloaded the scripts available within the Service Graph Connector for AWS. See [Download the AWS scripts](../task/sgc-cmdb-aws-scripts-dwld.md).

Decide the following details to be used later during the execution of the AWS scripts:

-   [ServiceNow IAM role](sgc-cmdb-aws-scripts-prereq.md#section_mxv_3l3_pzb)
-   [ServiceNow IAM username](sgc-cmdb-aws-scripts-prereq.md#section_sf3_rl3_pzb)
-   [S3 bucket for the ServiceNow IAM role](sgc-cmdb-aws-scripts-prereq.md#)

    **Note:** Define an S3 bucket only when you are using [deep discovery scripts](sgc-cmdb-aws-script-op.md#section_ahc_jwf_4zb).


## Determine the ServiceNow IAM role

Determine the identity and access management \(IAM\) role that performs read-only operations in member accounts to fetch the configuration items \(CIs\) from the AWS environment.

By default, the CreateSnowOrganizationAccountAccessRoleInMemberAccount.yml script creates the SnowOrganizationAccountAccessRole IAM role. You can use the default name created by the script or create a new IAM role. However, when required as an input parameter, you must enter the same IAM role across scripts. See [Executing scripts required for setting up AWS](sgc-cmdb-aws-script-op.md).

## Determine the ServiceNow IAM username

Determine the name of the IAM user that assumes the ServiceNow IAM role in the member accounts.

By default, the CreateServiceNowUser.yml script creates the NOWSGCUser IAM user. You can use the default name created by the script or create a new IAM user. However, when required as an input parameter, you must enter the same IAM username across scripts. See [Executing scripts required for setting up AWS](sgc-cmdb-aws-script-op.md).

## Define the S3 bucket for deep discovery

Set up an S3 bucket with read and delete privileges for the ServiceNow IAM role to store and delete the SendCommand API responses when importing AWS data.

### Before you begin

Role required: Application administrator

### About this task

Create an S3 bucket for the Service Graph Connector for AWS application and enable the ServiceNow IAM role to have access to this bucket in the organization.

**Note:** Use an S3 bucket only when you want to perform deep discovery on EC2 instances.

### Procedure

1.  Create an S3 bucket in an AWS account region.

    See [Creating a bucket](https://docs.aws.amazon.com/AmazonS3/latest/userguide/create-bucket-overview.html) on the AWS documentation site.

    **Note:** The S3 bucket must have the following permission settings.

    |Permission|Setting|
    |----------|-------|
    |Access|Bucket and objects not public|
    |S3 Block Public Access|Block public access to S3 buckets and objects|

    For more information, see [S3 Block Public Access](https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-control-block-public-access.html) on the AWS documentation site.

2.  Add a bucket policy.

    See [Bucket policies](https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucket-policies.html) on the AWS documentation site.

    To access the S3 bucket you created in [step 1](sgc-cmdb-aws-scripts-prereq.md#creates3bucket), its bucket policy must allow the IAM instance profile role attached to the managed EC2 instances. You can either create a bucket policy or grant access to your AWS member account in the bucket access control list \(ACL\). The member account must include the EC2 instances.

    **Note:** Adding an AWS member account to the bucket ACL allows all users and roles in the member account to access the S3 bucket.

    Refer to the following sample code when adding a bucket policy.

    ```
    {
        "Version": "2012-10-17",
        "Id": "S3PolicyforServiceNowIAMrole",
        "Statement": [
            {
                "Sid": "EC2S3Access",
                "Effect": "Allow",
                "Principal": {
                    "AWS": "arn:aws:iam::*AWS-ACCOUNT*:role/*INSTANCE-PROFILE-ROLE-NAME*"
                },
                "Action": [
                    "s3:GetObject",
                    "s3:PutObject",
                    "s3:PutObjectAcl"
                ],
                "Resource": "arn:aws:s3:::*DOC-EXAMPLE-BUCKET*/*"
            }
        ]
    }
    ```

    Where

    -   *SOURCE-AWS-ACCOUNT* is the AWS account ID of the member account that includes the EC2 instances.
    -   *INSTANCE-PROFILE-ROLE-NAME* is the IAM instance profile that is attached to the EC2 instances.

        By default, the AmazonSSMForInstancesRoleSetup.yml script creates the AmazonSSMForInstancesRole IAM instance profile role and attaches the role to the AmazonSSMManagedInstanceCore bucket policy. See [Executing scripts required for setting up AWS](sgc-cmdb-aws-script-op.md).

    -   *DOC-EXAMPLE-BUCKET* is the S3 bucket name.
    The following example bucket policy shows the effect, principal, action, and resource elements. The policy allows AmazonSSMRoleForInstances, an IAM instance profile role in an account with ID `123456789000`, `s3:GetObject`, `s3:PutObject`, and `s3:PutObjectAcl` S3 permissions on the `myS3Bucket` bucket.

    ```
    {
        "Version": "2012-10-17",
        "Id": "S3PolicyforServiceNowIAMrole",
        "Statement": [
            {
                "Sid": "EC2S3Access",
                "Effect": "Allow",
                "Principal": {
                    "AWS": [
                        "arn:aws:iam::123456789000:role/AmazonSSMRoleForInstances",
                        "arn:aws:iam::123456789001:role/AmazonSSMRoleForInstances",
                        "arn:aws:iam::123456789002:role/AmazonSSMRoleForInstances",
                        "arn:aws:iam::123456789003:role/AmazonSSMRoleForInstances",
                        "arn:aws:iam::123456789004:role/AmazonSSMRoleForInstances"
                    ]
                },
                "Action": [
                    "s3:GetObject",
                    "s3:PutObject",
                    "s3:PutObjectAcl"
                ],
                "Resource": "arn:aws:s3:::myS3Bucket/*"
            }
        ]
    }
    ```

3.  Attach IAM permissions to the instance profile role for EC2 instances to publish the SendCommand API responses to the S3 bucket you created in [step 1](sgc-cmdb-aws-scripts-prereq.md#creates3bucket).

    See [Using instance profiles](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use_switch-role-ec2_instance-profiles.html) and [Attach an IAM role to an instance](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/iam-roles-for-amazon-ec2.html#attach-iam-role) on the AWS documentation site.

    The IAM instance profile role attached to the managed EC2 instances must have the `s3:GetObject`, `s3:PutObject`, and `s3:PutObjectAcl` S3 permissions to allow access to the S3 bucket as shown in the following sample policy.

    ```
    {
        "Version": "2012-10-17",
        "Statement": [
            {
            "Sid": "PublishTerminalOutputToS3",
                "Effect": "Allow",
                "Action": [
                    "s3:PutObject",
                    "s3:GetObject",
                    "s3:PutObjectAcl"
                ],
                "Resource": "arn:aws:s3:::*DOC-EXAMPLE-BUCKET*/*"
            }
        ]
    }
    ```

    Where, *DOC-EXAMPLE-BUCKET* is the S3 bucket name.

    **Note:** Make sure you add the suffix `/*` at the end of the bucket name to enable creating files under the bucket name.


