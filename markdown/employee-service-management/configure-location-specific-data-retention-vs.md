---
title: Configure country-specific data retention settings for Vaccination Status
description: Configure the data retention settings for vaccine responses so your data retention policy is country-specific.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Vaccination Status, Safe Workplace, Health and Safety, Employee Service Management]
---

# Configure country-specific data retention settings for Vaccination Status

Configure the data retention settings for vaccine responses so your data retention policy is country-specific.

## Before you begin

Role required: sn\_imt\_core.admin, sn\_imt\_health\_test.admin, or sn\_imt\_vaccine.admin

## About this task

Employers remain solely responsible for complying with their legal obligations under applicable law, including data protection laws on collection, use, disclosure, and retention of personal data, and should enable, choose not to enable, or customize any functionality available within the application to meet the Employers’ specific requirements.

The **Vaccination Status data retention period \(in days\)** property sets the number of days that the user-reported vaccination status data is available in the Vaccine response table \[sn\_imt\_vaccine\_vaccine\_response\] before it is deleted automatically. The **Data Retention Job for Vaccination Status** scheduled job runs daily to delete records that have an updated date past the specified retention period.

**Note:** Any historical data retained for use in the Vaccination Status Dashboard is count data only. Personally identifying information is removed by default. If the vaccine responses are deleted before the duration is met, the reported statuses and attachments are deleted, too.

Enable the **Use country-specific data retention policy for Vaccination Status** property \[sn\_imt\_vaccine.use\_country\_specific\_data\_retention\_policy\] and use the Data Retention module in Employee Health and Safety Status to define policies at the country-level.

## Procedure

1.  Navigate to **All** &gt; **Vaccination Status** &gt; **Properties**.

2.  Set the **Use country-specific data retention policy for Vaccination Status** property to **true**.

3.  Click **Save**.

4.  Generate location policies for Vaccination Status.

    1.  Navigate to **Employee Health and Safety Status** &gt; **Data Retention**.

    2.  Click **Generate Location Policies**.

        The default number of days is based off the value in the **Vaccination Status data retention period \(in days\)** property.

5.  Open the location policy that you want to modify.

6.  Enter the number of days that you want to retain data for in the **Retention period \(in days\)** field.

7.  Click **Update**.


## Result

When the **Data Retention Job for Vaccination Status** daily scheduled job completes or is manually executed, the data of users in those locations have their records retained or deleted based on their country's data retention policy.

**Parent Topic:**[Vaccination Status](../concept/vaccination-status.md)

