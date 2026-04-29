---
title: Check External Key Management Service Key Status
description: View the status of your Amazon Web Services Key Management System \(AWS KMS\) key in your instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using External Key Management Service, External Key Management Service, Field Encryption, Encryption]
---

# Check External Key Management Service Key Status

View the status of your Amazon Web Services Key Management System \(AWS KMS\) key in your instance.

## Before you begin

Roles required: admin, security\_admin, and sn\_kmf.cryptographic\_manager

Verify that you have:

-   [Configured an External Key Management Service \(EKMS\) key definition.](ekms-configure-external-key-definition.md)
-   Security Admin or Crypto Manager role.

## About this task

You can check your AWS KMS key status at any time to verify its current state. Common scenarios for checking key status include resolving encryption failures, security audits, verifying synchronization after changes in AWS, or confirming your configuration before making updates.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption** &gt; **EKMS Configuration**.

2.  Open your EKMS configuration record.

3.  Locate the External Key Status field.

    The status field displays one of the following values:

    -   **Enabled**- Key is active and can be used for all encryption and decryption operations.
    -   **Disabled**- Key can't be used for encryption or decryption until re-enabled in AWS.
    -   **Pending deletion**- Key is scheduled for deletion and can't be used.
    -   **Deleted**- Key has been permanently deleted and can't be recovered.
    -   **Unavailable** - Your instance can't connect to AWS. This can be due to authentication issues with your EKMS configuration, network connectivity problems, or AWS service disruptions.
4.  Note the status and the last synchronization time.

    The automatic synchronization job runs every 30 minutes. The synchronization timestamp shows when the status was last updated from AWS. This default frequency is configurable if you need a different synchronization interval. See [Change synchronization frequency](ekms-change-synchronization-frequency.md).


## Result

You have verified your current AWS KMS key status. You can take appropriate action based on the status.

## What to do next

Based on the key status you see:

-   **Enabled**- No action required. Your key is operational.
-   **Disabled**- If this status is unexpected, check AWS KMS to determine why the key was disabled. This will trigger banner messages and a high-priority security task alerting you to the disabled key.
-   **Pending deletion**- If you must keep the key, cancel the scheduled deletion in AWS immediately. Immediate action is required to cancel the scheduled deletion or migrate from using this key, before the key is deleted.
-   **Deleted**- The key is permanently deleted. Data encrypted with this key can't be recovered. You must configure a new EKMS key.
-   **Unavailable**- Verify that your AWS service is up and accessible. Check the credentials in your EKMS configuration and use the Test button on the EKMS Configuration page to troubleshoot authentication and network connectivity issues.

**Important:** If your key is disabled or pending deletion, you must re-enable the key to create or update records in tables with encrypted field configurations.

**Parent Topic:**[Using External Key Management Service](../concept/ekms-using-external-key-management.md)

**Related topics**  


[Change the status of an AWS KMS Key](ekms-change-status-aws-kms-key.md)

