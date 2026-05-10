---
title: Support multiple jobs in a lifecycle event
description: Use the Jobs table to create lifecycle event cases where you can specify which job the case pertains to.
locale: en-US
release: australia
product: Lifecycle Events
classification: lifecycle-events
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Rehires, Transfers, Multiple jobs]
breadcrumb: [Using Lifecycle Events, Lifecycle Events, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Support multiple jobs in a lifecycle event

Use the Jobs table to create lifecycle event cases where you can specify which job the case pertains to.

## Before you begin

Role required: sn\_hr\_core.admin

For example, say that you have an intern that is being transferred to a full-time position. The intern has two associated job records. When an onboarding case for the full-time position is created, the case is associated with the full-time job record, ensuring that downstream activity sets and activities are triggered based on information from that relevant job record.

## About this task

Beginning in the New York release, you can use the new Jobs \(sn\_hr\_core\_job\) table to store multiple job records per user and capture the job history of users within your organization. See [Capturing multiple job records for a user](../concept/support-hr-users-with-multiple-jobs.md) for more information.

## Procedure

1.  If you are using an integration to pull HR profiles from a third-party system, configure your integration to pull jobs information into the Jobs \(sn\_hr\_core\_job\) table.

    For details on how to configure a third-party integration with HR Service Delivery, see [Integration of HR Service Delivery with third-party systems](../concept/integrate-third-party-systems.md).

2.  For HR case creation, associate the subject person's job to the HR case with the **subject\_person\_job** field.

    For example, for the preconfigured New Hire Onboarding lifecycle event, the **Create HR Case if Start Date is Future** business rule for the Jobs table is configured to automatically create onboarding cases for users with a future job start date. When the rule creates the onboarding case, it uses the **subject\_person\_job** field to specify which job the user is being onboarded for.

3.  For the lifecycle event, make sure that the relevant activity sets are triggered by the subject person's job by updating the **Trigger field** value to **subject\_person\_job**.

    For example, the Day 1 activity set in the preconfigured New Hire Onboarding lifecycle event is triggered by the subject person's job start date.

    ![A lifecycle event activity set with trigger field set to the subject person's job start date.](../image/multiple-jobs-le-activity-set-ex.png)

4.  If you are not using a third-party integration and need to configure the switch of a primary job, you can use the **Switch primary job** subflow to switch the subject person's primary job through a lifecycle event activity.

    For example, you can create a lifecycle event activity to switch the primary job of the subject person from the old to the new job by setting the **Activity type** value to **Flow** and the **Flow** value to **Switch primary job**.

    ![A lifecycle event activity with a flow to switch the primary job.](../image/multiple-jobs-switch-primary-job-ex.png)


**Related topics**  


[hr\_Utils - Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/hr_UtilsAPI.md)

[hr\_ActivitySet - Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/hr_ActivitySetAPI.md)

[hr\_ActivityUtils - Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/hr_ActivityUtilsAPI.md)

