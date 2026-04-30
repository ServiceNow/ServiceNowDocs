---
title: Exclude a resource from all Cloud Cost Management reports
description: To ensure that cost data for a particular resource doesn’t appear in a report, you exclude the resource by adding it to the Excluded Resources list.
locale: en-US
release: xanadu
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Exclude a resource from all Cloud Cost Management reports

To ensure that cost data for a particular resource doesn’t appear in a report, you exclude the resource by adding it to the Excluded Resources list.

## Before you begin

A cloud account \(parent account\) that has at least one service account and related datacenters is required.

Role required: insights\_admin \[sn\_clin\_core.insights\_admin\] or insights\_owner \[sn\_clin\_core.insights\_owner\] for owned service accounts.

## About this task

-   Excluding a resource from a report means that the resource doesn't get displayed in the report. This setting doesn’t affect analysis of data for the resource.
-   At any time, you can remove a resource from the Excluded Resources list.
-   An insights\_owner can exclude resources and remove a resource from the Excluded Resources list only in owned service accounts.
-   Production resources are examples of resources that you might exclude. Because production resources must always be active, you might, for example, want to exclude production resources from Business Hours reports.
-   You can exclude a resource either from a single report type or from all reports. You can select a resource and select **Exclude** for excluding the resource from the current report. The resource you exclude gets added to the **Excluded Resources** list for the report.

## Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Administration** &gt; **Global exclusions**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Resource|The resource to exclude. Only virtual machine resources appear in the list.|
    |Description|The reason for excluding the resource.|

4.  Select **Save**.


## Result

The resource is excluded from all reports. After you submit the record, you can open it to update the reports from which to exclude the resource.

-   **[Remove a resource from the Excluded Resources list](exclusion-list-remove-cloudin.md)**  
You can remove a resource from the Excluded Resources list.

**Parent Topic:**[Using Cloud Cost Management](../concept/using-cloud-insights.md)

