---
title: Prepare to run the Amazon S3 collector
description: Create an AWS IAM user with the permissions required for the metadata collector to harvest metadata from Amazon S3 buckets and objects.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/prepare-to-run-amazon-s3-collector.html
release: australia
topic_type: task
last_updated: "2026-06-18"
reading_time_minutes: 2
keywords: [Amazon S3, metadata collector, IAM user, access key, credentials, permissions]
breadcrumb: [Amazon S3 metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Prepare to run the Amazon S3 collector

Create an AWS IAM user with the permissions required for the metadata collector to harvest metadata from Amazon S3 buckets and objects.

## Before you begin

Role required: admin

## About this task

The collector authenticates to Amazon S3 using either an AWS credentials file or an access key ID and secret access key. Complete the following steps to create a dedicated IAM user, assign the required permissions, obtain an access key, and set up a credentials file.

## Procedure

1.  Create an IAM user for running the collector.

    1.  Log in to the [AWS portal](https://console.aws.amazon.com/) and navigate to the IAM service.
    2.  Under **Users**, select **Add users**.
    3.  Enter a name for the user and complete the user creation workflow.
2.  Assign the following permissions to the user.

    |Permission|AWS API|Object cataloged using the permission|
    |----------|-------|-------------------------------------|
    |`s3:ListAllMyBuckets`|[`ListBuckets`](https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListBuckets.html)|List of all buckets owned by the user|
    |`s3:GetBucketLocation`|[`GetBucketLocation`](https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketLocation.html)|The region the bucket resides in|
    |`s3:ListBucket`|[`ListObjectsV2Paginator`](https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListObjectsV2.html)|The list of objects within included buckets|
    |`s3:GetBucketVersioning`|[`GetBucketVersioning`](https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketVersioning.html)|The versioning state of the bucket|
    |`s3:GetBucketAcl`|[`GetBucketAcl`](https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketAcl.html)|The ACL \(access control list\) of the bucket|
    |`s3:GetObjectAcl`|[`GetObjectAcl`](https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObjectAcl.html)|The ACL \(access control list\) of the object|
    |`s3:GetObject`|[`HeadObject`](https://docs.aws.amazon.com/AmazonS3/latest/API/API_HeadObject.html)|The metadata of an object|

3.  Obtain an access key for the user.

    If you already have an access key for the user, skip this step. Detailed AWS documentation on this topic is [available in the AWS Tools for PowerShell documentation](https://docs.aws.amazon.com/powershell/latest/userguide/pstools-appendix-sign-up.html).

    1.  In the IAM service, under **Users**, select the user.
    2.  On the **Security credentials** tab, select **Create access key**.
    3.  Select **Application running outside AWS**, then select **Next**.
    4.  Enter an optional description tag, then select **Create access key**.
    5.  Copy the **Access key ID** and **Secret access key** values. You need these values when configuring the collector.
4.  Set up an AWS credentials file.

    If you already have the AWS CLI installed and a credentials profile file configured, skip this step.

    1.  Install the AWS CLI. For details, see the [AWS CLI installation documentation](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html).
    2.  From the command line, run [`aws configure`](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html).

        This command stores the credentials in `~/.aws/credentials`.


## Result

The IAM user has the permissions required to run the Amazon S3 metadata collector.

## What to do next

Use these credentials when configuring the collector. See [Create an Amazon S3 metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-amazon-s3-metadata-collector.md).

**Parent Topic:**[Amazon S3 metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/amazon-s3-metadata-collector.md)

