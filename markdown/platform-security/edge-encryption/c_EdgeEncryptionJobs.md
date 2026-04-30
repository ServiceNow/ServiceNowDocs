---
title: Repair or recover order-preserving encrypted data
description: If you have the security-admin role, you can schedule jobs performed by the Edge Encryption proxy to repair or recover fields that use order preserving encryption.You can schedule a job to find and repair fields where the order token is missing.Run this job when the proxy database has lost data. This job finds all records that have been encrypted with a token \(order preserving encryption type\) and sends them to the proxy so that the proxy database can be rebuilt.
locale: en-US
release: xanadu
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Edge Encryption, Edge Encryption, Encryption]
---

# Repair or recover order-preserving encrypted data

If you have the security-admin role, you can schedule jobs performed by the Edge Encryption proxy to repair or recover fields that use order preserving encryption.

Schedule jobs to:

-   Repair order tokens.
-   Recreate the proxy database.

Running these jobs can be a time-consuming operation that might impact the performance of the Edge Encryption proxy. Schedule these jobs at a time when no users or a minimum set of users are using the system, such as midnight on the weekend.

**Parent Topic:**[Configuring Edge Encryption](edge-config.md)

## Schedule an order token repair job

You can schedule a job to find and repair fields where the order token is missing.

### Before you begin

Role required: security\_admin

### About this task

Use these jobs to repair individual fields in a table or to repair all fields using order preserving encryption. Run this job when the proxy database has been offline while the instance has been running, which results in order preserving fields that are missing order tokens.

### Procedure

1.  Navigate to **All** &gt; **Edge Encryption Configuration** &gt; **Maintenance** &gt; **Schedule Order Token Repair**.

2.  Fill in the fields on the form, as appropriate.

    |Field|Value|
    |-----|-----|
    |Name|Enter a descriptive name.|
    |Job Type|Select **Order Token Repair**.|
    |All fields|Select this check box to repair all tables.|
    |Table|Select a table.|
    |Column|Select a column.|
    |Active|Clear this check box if you want to deactivate this job.|
    |Run|Select the period between job executions.|
    |Starting|Enter the date and time to run the job for the first time.|

3.  Click the menu icon in the form header and select **Save**.

4.  To see an estimated count of records to be updated, click **Estimated Record Count**.


## Schedule a proxy-database recovery job

Run this job when the proxy database has lost data. This job finds all records that have been encrypted with a token \(order preserving encryption type\) and sends them to the proxy so that the proxy database can be rebuilt.

### Before you begin

Role required: security\_admin

### Procedure

1.  Navigate to **All** &gt; **Edge Encryption Configuration** &gt; **Maintenance** &gt; **Schedule Database Recovery**.

2.  Fill in the fields on the form, as appropriate.

    |Field|Value|
    |-----|-----|
    |Name|Enter a descriptive name for this job.|
    |Job Type|Select **Database Recovery**.|
    |Active|Clear this check box if you want to deactivate this job.|
    |Run|Select the period between job executions.|
    |Starting|Enter the date and time to run this job for the first time.|

3.  Click the menu icon in the form header and select **Save**.

4.  To see an estimated count of records to be updated, click **Estimate Record Count**.


