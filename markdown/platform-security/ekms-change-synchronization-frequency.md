---
title: Change synchronization frequency
description: Modify the system property to change how often External Key Management Service \(EKMS\) synchronizes Amazon Web Service Key Management Service \(AWS KMS\) key status with your instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-31"
reading_time_minutes: 1
breadcrumb: [Using External Key Management Service, External Key Management Service, Field Encryption, Encryption]
---

# Change synchronization frequency

Modify the system property to change how often External Key Management Service \(EKMS\) synchronizes Amazon Web Service Key Management Service \(AWS KMS\) key status with your instance.

## Before you begin

Role required: admin, security\_admin

## About this task

By default, EKMS synchronizes AWS KMS key status every 30 minutes through a background job. You can change this frequency to meet your organization's needs by modifying a system property. The synchronization job updates your instance with any key state changes in AWS \(enabled, disabled, pending deletion, deleted\).

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  In the system properties list, search for and open the `com.glide.encryption.ekms.scheduler.health_check_interval` property.

3.  Set the value to the synchronization interval you want to use, in minutes.

    The default value is 30 minutes. Consider your organization's security requirements when setting the interval. A shorter interval provides faster detection of key status changes.

4.  Select **Save**.


## Result

The synchronization frequency is updated. The background job will now run at your specified interval to check AWS key status.

## What to do next

After changing the frequency, monitor the synchronization job to verify it runs at the new interval.

**Note:** The next synchronization will occur based on your new interval setting.

**Parent Topic:**[Using External Key Management Service](../concept/ekms-using-external-key-management.md)

