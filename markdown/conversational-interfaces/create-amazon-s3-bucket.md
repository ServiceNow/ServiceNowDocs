---
title: \(Legacy\) Create an Amazon S3 bucket
description: Create an Amazon S3 bucket to store the files required for configuring Conversational IVR within your AWS account.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/create-amazon-s3-bucket.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure your AWS account, Configure, Conversational IVR with Amazon Connect, Integrate VA for NLU with voice channels, Virtual Agent channel integrations, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Create an Amazon S3 bucket

Create an Amazon S3 bucket to store the files required for configuring Conversational IVR within your AWS account.

## Before you begin

Role required: admin

**Note:** Before creating the Amazon S3 Bucket, ensure that you have downloaded the `Lambda function`, `Lex Bot`, and `HelperLambda` files from this [Knowledge Base article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1430643).

For additional information about Amazon S3 Buckets, refer to the [Amazon S3 documentation](https://docs.aws.amazon.com/opsworks/latest/userguide/using-s3-bucket.html).

## Procedure

1.  Log in to the AWS Admin Console.

2.  Navigate to **Amazon S3** and click **Create bucket**.

3.  Provide a **Bucket name** \(for example: sn-ci-cc-amazon-connect-setup\) and note it down.

    This Bucket name will be used during the creation of a CloudFormation Stack at a later stage.

4.  Select the **AWS Region** from the drop-down and ensure that this region remains consistent throughout the setup process.

5.  Click **Create bucket**.

    You will be redirected to the list of Amazon S3 buckets that you have on your instance.

6.  Search for the bucket that you created and click the bucket name to open it.

    Clicking the bucket name takes you to the **Objects** tab of the bucket.

7.  On the Objects tab, click **Upload**.

8.  Click **Add Files** and browse for the following downloaded files:

    -   Lambda function
    -   Lex Bot
    -   HelperLambda
    -   Prompt

        **Note:**

        -   The Prompt file is not provided by ServiceNow. You must create your own Prompt file, note its name, and provide the name while creating the CloudFormation Stack. For more information about creating a Prompt, see [https://docs.aws.amazon.com/connect/latest/adminguide/prompts.html](https://docs.aws.amazon.com/connect/latest/adminguide/prompts.html).
        -   Also make sure that you do not rename any files while uploading them.
9.  Select all the files that you uploaded and select **Upload**.

    Once the files are uploaded, you will receive the

    ```
    Upload succeeded
    ```

    message.


**Parent Topic:**[\(Legacy\) Configuring your AWS account for use with Conversational IVR](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-aws-account.md)

