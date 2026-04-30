---
title: Populate SAP Concur report and metadata
description: As an administrator, fetch the reports metadata from other business applications such as SAP Concur. View the Concur expense reports, itemizations, and receipts from your ServiceNow instance.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Approvals hub integration with SAP Concur, Approval hub integrations, Approvals hub, Setup task management, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Populate SAP Concur report and metadata

As an administrator, fetch the reports metadata from other business applications such as SAP Concur. View the Concur expense reports, itemizations, and receipts from your ServiceNow instance.

## Before you begin

Role required: sp\_admin and sn\_hr\_integr\_fw.admin

## About this task

When you sync requests, you can view, track, and manage the pending requests from SAP Concur right from Employee Center Pro.

## Procedure

1.  Use one of the following methods to fetch the data.

    1.  Navigate to **All** &gt; **Integrations Framework** &gt; **Source**, select **Concur Integration**, and click **Run Job** to fetch Concur expenses report.

        This job uses the **Fetch concur reports** service to fetch the user and report data using the available **Get concur reports** flow.

    2.  Navigate to **System definition** &gt; **Scheduled jobs** and run the **Pull concur reports** job to sync the updates automatically on a configured schedule or need-basis.

    By default, Concur reports are synced daily and the last three months data is fetched. Admin can configure the frequency of the schedule job.

    **Note:** To ensure you have the latest data from Concur, the daily scheduled job fetches the new records and any changes to the existing records.

2.  Verify the progress of the job from **All** &gt; **Integrations Framework** &gt; **Job Tracker.**

3.  Check the populated data from the following tables:

    -   Concur Expense Report Staging \(sn\_ex\_cnc\_concur\_report\_staging\)​​
    -   Concur Expense Report \(sn\_ex\_cnc\_concur\_report\)​​
    -   ​Concur User Mappings \(sn\_sap\_concur\_spok\_sap\_concur\_user\_mappings\)​
    -   Concur Sync Details \(sn\_ex\_cnc\_concur\_sync\_details\)​
    -   ​Concur Expense Entry \(sn\_ex\_cnc\_concur\_expense\)​
    -   Concur Comments \(sn\_ex\_cnc\_concur\_comment\)
    **Note:** Concur Expense Entry and Concur Comments data is populated real-time when the approver clicks the open request on the **My tasks** page.

    The tables show the expense reports and related metadata. See the sample Concur expense report and its metadata.![Sample expense report](../images/c-sample-concur-report.png).

    If reports do not appear on the Concur Expense Report \(sn\_ex\_cnc\_concur\_report\)​​, check the credentials \(oauth\_2\_0\_credentials\) with names **SAP Concur** and **SAP Concur v4 Credentials**. If credentials are fine, check **Get concur reports** flow execution for more information.


## Result

The SAP Concur integration syncs the requests automatically and displays the pending open requests on **My tasks**.

## What to do next

You can navigate to **All** &gt; **Employee Center** &gt; **SAP Concur Spoke** &gt; **Concur Sync Details** to check the timestamp of the last sync.

-   Only the open requests are displayed on the approvers **My tasks** page.
-   Changes to the reports and requests reflect when the approver selects the open task.
-   \(Optional\) You can disable the scheduled job by marking the job inactive from **System Definition** &gt; **Scheduled job**.

Proceed to To-dos Configuration and use the default **Approval \| SAP Concur** task configuration.

**Parent Topic:**[Approvals hub integration with SAP Concur](../concept/x-concur-sa-integration.md)

