---
title: Configure Amazon S3 for external content indexing
description: Create an Identity and Access Management \(IAM\) user in the Amazon Web Services \(AWS\) Management Console. Define an access key for your new user to allow the Amazon S3 external content connector to access your Amazon S3 source system.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-11-14"
reading_time_minutes: 6
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Amazon S3 external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure Amazon S3 for external content indexing

Create an Identity and Access Management \(IAM\) user in the Amazon Web Services \(AWS\) Management Console. Define an access key for your new user to allow the Amazon S3 external content connector to access your Amazon S3 source system.

## Before you begin

You need AWS Management Console credentials for your AWS account. You must have sufficient privileges to create an IAM user, define policy permissions for that user, and create an access key for that user. To learn more about these tasks, see the Amazon Web Services [IAM users](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_users.html), [Define custom IAM permissions with customer managed policies](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_create.html), [Permissions required to access IAM resources](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_permissions-required.html), [Manage access keys for IAM users](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html), and [Secure access keys](https://docs.aws.amazon.com/IAM/latest/UserGuide/securing_access-keys.html) resources.

Role required: none

## About this task

The Amazon S3 external content connector retrieves content from buckets in your Amazon S3 source system using the Amazon Web Services \(AWS\) API. To access your Amazon S3 buckets, the connector uses an access key ID and secret access key that you define for a new Identity and Access Management \(IAM\) user. You specify bucket access permissions for this IAM user with an IAM policy.

Your ServiceNow AI Platform needs this IAM user's access key ID and secret access key to configure the Amazon S3 external content connector for proper connection to your AWS account.

**Important:** All content the connector retrieves from your Amazon S3 buckets is treated as public content, searchable by everyone who has access to your configured AI Search experience.

## Procedure

1.  Create a new IAM policy that defines permissions needed for the Amazon S3 external content connector user.

    1.  Log in to the Identity and Access Management page of the AWS Management Console at [https://console.aws.amazon.com/iam/](https://console.aws.amazon.com/iam/).

    2.  Navigate to **Access management** &gt; **Policies**, then select **Create policy**.

        ![Policies page in AWS Management Console IAM web service.](../image/aws-mc-iam-create-policy.png)

    3.  In the Policy editor, select **JSON**, then paste the following JSON-format policy description into the editor, replacing the default policy description:

        ```json
        {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Sid": "ListAllBuckets",
              "Effect": "Allow",
              "Action": [
                "s3:ListAllMyBuckets"
              ],
              "Resource": [
                "*"
              ]
            },
            {
              "Sid": "BucketCrawlPermissions",
              "Effect": "Allow",
              "Action": [
                "s3:ListBucket",
                "s3:GetBucketLocation"
              ],
              "Resource": [
                "arn:aws:s3:::example-bucket-1",
                "arn:aws:s3:::example-bucket-2"
              ]
            },
            {
              "Sid": "ObjectCrawlPermissions",
              "Effect": "Allow",
              "Action": [
                "s3:GetObject"
              ],
              "Resource": [
                "arn:aws:s3:::example-bucket-1/*",
                "arn:aws:s3:::example-bucket-2/*"
              ]
            }
          ]
        }
        ```

        ![Specify permissions page for new policy in AWS Management Console IAM web service.](../image/aws-mc-iam-json-policy-editor.png)

    4.  In the Policy editor, update the `Resource` array for the `BucketCrawlPermissions` object to include Amazon Resource Names \(ARNs\) for all of the Amazon S3 buckets you want the external content connector to be able to crawl.

        This array should only contain ARNs for the Amazon S3 bucket resource type. For details on ARNs, see [https://docs.aws.amazon.com/IAM/latest/UserGuide/reference-arns.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference-arns.html). To learn more about resource types defined for Amazon S3, see [https://docs.aws.amazon.com/service-authorization/latest/reference/list\_amazons3.html\#amazons3-resources-for-iam-policies](https://docs.aws.amazon.com/service-authorization/latest/reference/list_amazons3.html#amazons3-resources-for-iam-policies). When granting access to your Amazon S3 buckets, remember that all content crawled by the connector is searchable by everyone who has access to your configured AI Search experience.

    5.  In the Policy editor, update the `Resource` array for the `ObjectCrawlPermissions` object to include ARNs for all of the Amazon S3 resources you want the external content connector to be able to retrieve.

        This array should only contain ARNs for the Amazon S3 object resource type. You can use wildcards to grant access to all objects in a bucket, as shown in the example ARNs. For details on ARNs, see [https://docs.aws.amazon.com/IAM/latest/UserGuide/reference-arns.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference-arns.html). To learn more about resource types defined for Amazon S3, see [https://docs.aws.amazon.com/service-authorization/latest/reference/list\_amazons3.html\#amazons3-resources-for-iam-policies](https://docs.aws.amazon.com/service-authorization/latest/reference/list_amazons3.html#amazons3-resources-for-iam-policies). When granting access to your Amazon S3 bucket resources, remember that all content crawled by the connector is searchable by everyone who has access to your configured AI Search experience.![Detail of JSON policy showing Resource arrays for policy objects in AWS Management Console IAM web service.](../image/aws-mc-iam-json-policy-resource-arrays.png)

    6.  Select **Next**.

    7.  On the Review and create page, enter a **Policy name** and optionally a **Description** for your new policy, then select **Create policy**.

        As an example, you might enter `Amazon-S3-external-content-connector` as the policy name and `IAM policy with permissions for the ServiceNow Amazon S3 external content connector user.` as the definition.![Review and create page for new policy in AWS Management Console IAM web service.](../image/aws-mc-iam-policy-review-create.png)

    A message confirms that your new IAM policy was created successfully, and the policy appears in the list of IAM policies.![Policies list showing newly created policy in AWS Management Console IAM web service.](../image/aws-mc-iam-policies-list.png)

2.  Create a new IAM user in your AWS account:

    1.  In the Identity and Access Management page of the AWS Management Console, navigate to **Access management** &gt; **Users**, then select **Create user**.

        ![Users page in AWS Management Console IAM web service.](../image/aws-mc-iam-create-user.png)

    2.  On the Specify user details page, enter a name for your new IAM user, then select **Next**.

        As an example, you might enter `Amazon-S3-external-content-connector-user`.![Specify user details page for new user in AWS Management Console IAM web service.](../image/aws-mc-iam-specify-user-details.png)

    3.  On the Set permissions page, select **Attach policies directly** in the Permissions options section.

    4.  In the Permissions policies list, select the option for the new IAM policy that you created in step [1](configure-amazon-s3-external-content-indexing.md#create-iam-policy-step), then select **Next**.

        ![Set permissions page for new user in AWS Management Console IAM web service.](../image/aws-mc-iam-set-permissions-user.png)

    5.  On the Review and create page, select **Create user**.

        ![Review and create page for new user in AWS Management Console IAM web service.](../image/aws-mc-iam-user-review-create.png)

    A message confirms that your new IAM user was created successfully, and the user appears in the list of IAM users.![Users list showing newly created user in AWS Management Console IAM web service.](../image/aws-mc-iam-users.png)

3.  Create an access key for your new IAM user:

    1.  Select **View user** in the message that appeared when you completed step [2](configure-amazon-s3-external-content-indexing.md#create-iam-user-step).

        If the message and **View user** link are no longer visible, navigate to **Access management** &gt; **Users** in the AWS Management Console, then select the user that you created in step [2](configure-amazon-s3-external-content-indexing.md#create-iam-user-step).

    2.  In the Security credentials tab, navigate to the Access keys section and select **Create access key**.

        ![User editor for new user with Security credentials tab shown in AWS Management Console IAM web service.](../image/aws-mc-iam-user-create-access-key.png)

    3.  On the Access key best practices &amp; alternatives page, select the **Application running outside AWS** use-case, then select **Next**.

        ![Access key best practices & alternatives page for new access key in AWS Management Console IAM web service.](../image/aws-mc-iam-access-key-use-case.png)

    4.  Enter a description tag value for your new access key.

        As an example, you might enter `Access key for the ServiceNow Amazon S3 external content connector user.`

    5.  Select **Create access key**.

        ![Set description tag page for new access key in AWS Management Console IAM web service.](../image/aws-mc-iam-access-key-description-tag.png)

        A message confirms that your new access key was created.

    6.  On the Retrieve access keys page, copy the new key's **Access key** and **Secret access key** values and store them in a secure location.

        ![Retrieve access keys page for new access key in AWS Management Console IAM web service.](../image/aws-mc-iam-access-key-retrieve.png)

        **Important:** Your connector admin needs this access key and secret access key when configuring the Amazon S3 external content connector.

    7.  Select **Done**.


## What to do next

Provide the IAM user access key and secret access key that you copied in step [3.f](configure-amazon-s3-external-content-indexing.md#copy-access-key-step) to your ServiceNow AI Platform admins. Your admin needs these items to configure an Amazon S3 external content connector to retrieve searchable content and security principals from your Amazon S3 buckets.

For details on creating and configuring an Amazon S3 external content connector, see [Create an Amazon S3 external content connector](create-ext-cont-connector-amazon-s3.md).

**Parent Topic:**[Amazon S3 external content connector](../concept/amazon-s3-external-content-connector.md)

