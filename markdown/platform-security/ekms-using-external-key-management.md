---
title: Using External Key Management Service
description: Manage and maintain your External Key Management Service \(EKMS\) configuration after initial setup
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-14"
reading_time_minutes: 2
breadcrumb: [External Key Management Service, Field Encryption, Encryption]
---

# Using External Key Management Service

Manage and maintain your External Key Management Service \(EKMS\) configuration after initial setup

## What you can do

Once EKMS is configured, you perform ongoing management tasks to maintain your encryption infrastructure. These operational tasks include managing AWS key status, monitoring synchronization, and updating access policies as your organization's needs change.

## Common tasks

Use EKMS to perform the following operational tasks:

-   Monitor key status synchronization between AWS and ServiceNow.
-   Verify the background synchronization job runs successfully.
-   Review access policies as organizational roles change.
-   Test encryption functionality after key status changes.
-   Coordinate key changes with application teams and administrators.

Use the related links to find information related to these common EKMS tasks.

## Key status impact

AWS KMS key status directly affects encryption and decryption operations in ServiceNow. When you change a key's status in AWS, EKMS synchronizes the change automatically every 30 minutes. Understanding how status changes impact your data access is critical for maintaining operations. This default frequency is configurable if you need a different synchronization interval. See [Change synchronization frequency](../task/ekms-change-synchronization-frequency.md).

## Automatic key wrapping after AWS key rotation

When you rotate your AWS KMS key, EKMS automatically detects the rotation and rewraps your External Key Encryption Key \(EKEK\). The EKEK itself isn't rotated, and your Data Encryption Keys \(DEKs\) remain unchanged. Only the wrapping layer is updated with the rotated AWS key.

This automatic process:

-   Maintains the security of your encryption chain.
-   Requires no manual intervention.
-   Causes no service interruption.
-   Typically completes within 30 minutes when the synchronization job runs.

-   **[Change the status of an AWS KMS Key](../task/ekms-change-status-aws-kms-key.md)**  
Modify the status of your Amazon Web Services Key Management System \(AWS KMS\) key and synchronize the status with your ServiceNow instance.
-   **[Check External Key Management Service Key Status](../task/ekms-check-key-status.md)**  
View the status of your Amazon Web Services Key Management System \(AWS KMS\) key in your instance.
-   **[Change synchronization frequency](../task/ekms-change-synchronization-frequency.md)**  
Modify the system property to change how often External Key Management Service \(EKMS\) synchronizes Amazon Web Service Key Management Service \(AWS KMS\) key status with your instance.
-   **[External Key Management Service and instance automation](../reference/ekms-instance-automation.md)**  
Understand requirements and limitations for instance automation operations when External Key Management Service is enabled.

**Parent Topic:**[External Key Management Service](ekms-external-key-management.md)

**Related topics**  


[External Key Management Service](ekms-external-key-management.md)

[Change the status of an AWS KMS Key](../task/ekms-change-status-aws-kms-key.md)

[Check External Key Management Service Key Status](../task/ekms-check-key-status.md)

