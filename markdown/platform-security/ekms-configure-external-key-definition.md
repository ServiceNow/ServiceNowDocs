---
title: Configure an external key definition
description: Configure your external encryption key to use in External Key Management Service \(EKMS\).
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring External Key Management Service, External Key Management Service, Field Encryption, Encryption]
---

# Configure an external key definition

Configure your external encryption key to use in External Key Management Service \(EKMS\).

## Before you begin

Roles required: admin, security\_admin, and sn\_kmf.cryptographic\_manager

**Note:** To configure EKMS, verify that you have an enabled key with your external key management provider, and the configured user has the necessary permissions to use the key.

The user must have permissions to run the following AWS KMS API operations:

-   kms:DescribeKey
-   kms:Encrypt
-   kms:Decrypt

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption** &gt; **EKMS Configurations** &gt; **New**.

2.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Application|Automatically populated with **Global**.|
    |Cloud KMS Provider|Automatically populated with **AWS**.|
    |EKMS Integration Name|Choose a name for the key definition. This name is referenced when running scripts.|
    |Key Region|Enter the key region associated with your external key. Example: ex. us-east-2.|
    |External Key Identifier|Enter the Amazon Resource Name \(AWS ARN\) for your external key.|
    |Primary Region URL|Enter the unique Primary Regional URL that begins with KMS. Example: https://kms.\[key region\]\_amazonaws.com.|
    |KMS Credentials Access Key|Enter the key management service \(KMS\) for your credentialed AWS user.|
    |KMS Credentials Secret Key|Enter the secret key for your credentialed AWS user.|

3.  Select **Submit**.


## Result

The external key definition is configured. Verify that the key status displays as Active for the new configuration. To confirm if the key is usable, select **Test EKMS Config**. Wait for the key status to change to Active before using it.![External Key Management Service key definition with an active status](../image/ekms-active-key-definition.png)

## What to do next

Next steps:

-   [Create a cryptographic module with external key wrapping](ekms-create-crypto-module.md)
-   [Create encrypted field configurations to specify which tables and columns to encrypt](ekms-create-encrypted-field-config.md)
-   [Set up module access policies to control who can view the encrypted data](ekms-set-up-maps.md)
-   [Test an external key definition](ekms-test-external-key-definition.md)

**Parent Topic:**[Configuring External Key Management Service](../concept/ekms-configuring-external-key-management.md)

