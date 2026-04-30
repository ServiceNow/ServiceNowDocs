---
title: Schedule import set jobs to pull data from the CRM system
description: Schedule import set jobs to pull sales representatives and associated sales accounts and active opportunities data from the CRM system into the ServiceNow instance.
locale: en-US
release: zurich
product: Legal Simple Contracts
classification: legal-simple-contracts
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Legal Simple Contracts, Configure, Legal Simple Contracts, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Schedule import set jobs to pull data from the CRM system

Schedule import set jobs to pull sales representatives and associated sales accounts and active opportunities data from the CRM system into the ServiceNow instance.

## Before you begin

[Configure Microsoft Dynamics CRM for sales contracts](integrate-legal-ms-dynamics-crm.md).

Role required: admin

## About this task

-   By default, the import set job is scheduled to run daily to pull the data from the CRM system.
-   Only active sales representatives and opportunities are pulled from the CRM system. All opportunities that are not won or lost are considered as active opportunities.​
-   When an opportunity is closed and not associated in any other active legal requests, the scheduled job will remove the opportunity record from the ServiceNow instance.

The import set jobs trigger a Workflow Studio flow that pulls the data from the CRM system into the ServiceNow instance. The maximum number of records pulled each time the job runs is based on the following Workflow Studio properties:

-   **The maximum number of records to return when fetching data** \(**sn\_flow\_designer.action\_picker\_limit**\)
-   **The maximum amount of iterations that a loop will run in flow designer** \(**sn\_flow\_designer.max\_iterations**\)

Based on the number of records pulled for your system, you can modify the values of these properties. For more information, see [Workflow Studio system properties](https://www.servicenow.com/docs/access?context=flow-designer-system-properties&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Administration** &gt; **Scheduled Imports**.

2.  Open a scheduled data imports record to update.

    The following scheduled data import jobs for pulling data from the CRM system are available:

    -   **Sales Representatives Scheduled Data Import**
    -   **Sales Accounts Scheduled Data Import**
    -   **Sales Opportunities Scheduled Data Import**
    For more information, see [Scheduled data imports](../reference/installed-with-legal-simple-contracts.md#section_scheduled_jobs)

3.  Configure the data import job as needed.

    For more information on configuring a data import set schedule, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) .

4.  To pull data from a different set of fields from the CRM system, update the corresponding transformation maps.

    For more information on configuring a transformation map, see [Create a transform map](https://www.servicenow.com/docs/access?context=t_CreateATransformMap&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) .


