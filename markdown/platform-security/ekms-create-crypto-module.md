---
title: Create a cryptographic module with external key wrapping
description: Create a cryptographic module that uses external Amazon Web Services Key Management System \(AWS KMS\) key wrapping to encrypt ServiceNow data.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring External Key Management Service, External Key Management Service, Field Encryption, Encryption]
---

# Create a cryptographic module with external key wrapping

Create a cryptographic module that uses external Amazon Web Services Key Management System \(AWS KMS\) key wrapping to encrypt ServiceNow data.

## Before you begin

Roles required: admin, security\_admin, and sn\_kmf.cryptographic\_manager

## About this task

A cryptographic module with external key wrapping generates encryption keys that are wrapped \(encrypted\) by your AWS KMS key in addition to ServiceNow's internal key management. ServiceNow can't decrypt your data without access to your external AWS key.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption Modules**.

2.  Select **New**.

3.  Enter a name for the module in the **Name** field.

4.  Select the **External wrap key** check box.

    **Important:** If **Externally Wrap Key** isn't selected, the module uses ServiceNow key wrapping, which doesn't use your AWS KMS key.

5.  In the **External KMS Configuration** field, enter or use the search function to select your EKMS configuration.![Enable the External Wrap Key option on a cryptographic module and select your External Key Management Service (EKMS) configuration.](../image/ekms-crypto-module.png)

6.  Select **Submit** to save the cryptographic module.


## Result

The cryptographic module is created and ready to be used for encrypting Field Encryption data.

When you enable external key wrapping on an existing cryptographic module, all keys for this module are automatically rewrapped with your External Key Encryption Key \(EKEK\). This protects them with your EKMS key. Both existing keys and future keys you create will be externally wrapped.

A security task is created to track the rewrapping process. To monitor the status, navigate to **All** &gt; **Security Center** &gt; **Security Task Manager** and look for the task with description 'Module key rewrap process for crypto module \[module\_id\]'. See [Security Tasks](../../security-center/concept/security-task-manager.md).

## What to do next

Next steps:

-   [Create encrypted field configurations to specify which tables and columns to encrypt](ekms-create-encrypted-field-config.md)
-   [Set up module access policies to control who can view the encrypted data](ekms-set-up-maps.md)

**Parent Topic:**[Configuring External Key Management Service](../concept/ekms-configuring-external-key-management.md)

