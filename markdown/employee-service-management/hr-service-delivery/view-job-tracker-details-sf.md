---
title: View job tracker details
description: Track every pull that has been performed from ServiceNow to SuccessFactors either by schedule job or manual reconciliation process. View details of the job, such as when did the job begin and end, when did the records start loading into staging tables, or did the job run completely or fail in between.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using HR Service Delivery Integration with SuccessFactors, HR Service Delivery Integration with SuccessFactors, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# View job tracker details

Track every pull that has been performed from ServiceNow to SuccessFactors either by schedule job or manual reconciliation process. View details of the job, such as when did the job begin and end, when did the records start loading into staging tables, or did the job run completely or fail in between.

## Before you begin

Role required: sn\_hr\_sf.admin

## Procedure

1.  Navigate to **All** &gt; **Integrations Framework** &gt; **Job Tracker**.

2.  Open **SAP SuccessFactors**.

3.  View job details:

    |Field|Description|
    |-----|-----------|
    |Job name|Name of the job that has run.|
    |Job start time|Date and time when the job started.|
    |Job end time|Date and time when the job ended.|
    |Source|Origin of the job.|
    |State|Current state of the job such as **Complete** or **Failed**.|
    |Error message|Message displayed when the job fails.|

4.  Select a job record.

    In the Integration Service Job Trackers related list, view the service job details.

    |Field|Description|
    |-----|-----------|
    |Name|Unique identifier for the service job run.|
    |Service type|Name of the service job that has run. For example, Worker Profiles integration service.|
    |Flow|Flow of the job.|
    |Import set tables|Available staging tables.|
    |Active|Option that indicates if the state of the job tracker is active.|
    |Application|Application containing the record.|
    |Source|Source of the integration service|
    |Order|Order in which the item is executed as part of sync.|


**Parent Topic:**[Using HR Service Delivery Integration with SuccessFactors](using-hr-service-delivery-integration-with-success-factors.md)

**Related topics**  


[View to dos](../task/view-to-dos-sf.md)

[Use transform maps](../reference/use-transform-maps-sf.md)

[Field mappings](../reference/field-mappings-sf.md)

[Now Assist Virtual Agent topics for HR Service Delivery Integration with SuccessFactors](na-va-sf.md)

[Use HCM AI agents for HR Service Delivery Integration with SuccessFactors](conversational-agents-sf.md)

