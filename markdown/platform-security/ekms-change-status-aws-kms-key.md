---
title: Change the status of an AWS KMS Key
description: Modify the status of your Amazon Web Services Key Management System \(AWS KMS\) key and synchronize the status with your ServiceNow instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using External Key Management Service, External Key Management Service, Field Encryption, Encryption]
---

# Change the status of an AWS KMS Key

Modify the status of your Amazon Web Services Key Management System \(AWS KMS\) key and synchronize the status with your ServiceNow instance.

## Before you begin

Roles required: admin, security\_admin, and sn\_kmf.cryptographic\_manager

Verify that you have:

-   Configured an External Key Management Service \(EKMS\) in ServiceNow
-   Permissions to modify key status in AWS

## About this task

AWS KMS keys can have different statuses that control whether they can be used for encryption and decryption operations. Changing a key's status in AWS affects your ability to encrypt new data and decrypt existing data in External Key Management Service \(EKMS\). A background synchronization job updates EKMS with the current AWS key status every 30 minutes.

**Important:** Key status changes have immediate security and operational impacts. Coordinate all key status changes with your ServiceNow administrators and application teams before making changes.

## Procedure

1.  Access AWS Key Management Service.

2.  Review the current key status.

3.  Change the key status based on your requirements.

    **Warning:** Disabling or deleting a key will prevent ServiceNow from encrypting new data and decrypting existing data. Verify that you have a plan for data migration or key recovery before disabling or scheduling deletion.

4.  Wait for the scheduled synchronization job to process the key status change.

    EKMS automatically synchronizes AWS key status every 30 minutes through a background job. The job will detect and update the key status change in your instance within 30 minutes.

5.  Verify the key status updated in EKMS.

    See [Check External Key Management Service key status](ekms-check-key-status.md).

    The AWS key status is synchronized with EKMS.


## Result

The new status is reflected in your EKMS configuration, and encryption and decryption operations behave according to the new key status.

When you disable a key in AWS, ServiceNow provides multiple notifications to alert administrators:

-   The External Key Status field changes to "Disabled" on the EKMS Configuration page.
-   A high-priority security task is automatically created in Security Center notifying administrators that the EKMS key was disabled. To view notifications, navigate to **All** &gt; **Security Center** &gt; **Overview**. See [Security Center](../../security-center/concept/sec-center-v2.md).

While the key is disabled, you can't encrypt or decrypt data in encrypted fields. You can still create records if the encrypted field isn't a required field, and you can update non-encrypted fields in existing records. All cryptographic operations are blocked until the key is re-enabled in AWS.

## What to do next

Important considerations after changing key status:

-   **If you disabled your AWS key:** New data cannot be encrypted, and existing encrypted data cannot be decrypted until the key is re-enabled. Plan for how encrypted fields should be handled during this time.
-   **If you enabled a previously disabled key:** Encryption and decryption operations resume once the synchronization job updates the key status in EKMS \(within 30 minutes\). Test your EKMS Configuration by clicking the **Test** button. Then verify that all encrypted fields are accessible.
-   **If you scheduled the key for deletion:** You have 7 to 30 days \(depending on your deletion schedule within AWS\) to cancel the deletion before the key is permanently deleted. After permanent deletion, encrypted data can't be recovered.
-   **If you canceled a scheduled deletion:** Remember to enable the key if it was disabled. Canceling deletion does not automatically enable the key.

**Important:** The automatic synchronization job runs every 30 minutes. EKMS automatically detects status changes within 30 minutes of when they occur in AWS.

AWS requires a minimum 7-day waiting period for key deletion. During this period, the key status shows as "Pending deletion" in both AWS and EKMS. Keys can't be used while pending deletion. After seven days, the key is permanently deleted and can't be recovered. All data encrypted with a deleted key becomes permanently inaccessible.

**Parent Topic:**[Using External Key Management Service](../concept/ekms-using-external-key-management.md)

**Related topics**  


[External Key Management Service](../concept/ekms-external-key-management.md)

[Configure an external key definition](ekms-configure-external-key-definition.md)

[Check External Key Management Service Key Status](ekms-check-key-status.md)

