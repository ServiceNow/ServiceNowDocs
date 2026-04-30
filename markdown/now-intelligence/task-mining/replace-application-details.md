---
title: Avoid capturing and displaying application details
description: Prevent the Task Mining agent from collecting application details by replacing application details that match event filters. Application details include the application name, URL, and window name that appear during application categorization and in dashboards.
locale: en-US
release: zurich
product: Task Mining
classification: task-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Task Mining, Platform Analytics]
---

# Avoid capturing and displaying application details

Prevent the Task Mining agent from collecting application details by replacing application details that match event filters. Application details include the application name, URL, and window name that appear during application categorization and in dashboards.

## Before you begin

Role required: sn\_tm\_core.power\_user, sn\_tm\_core.admin

## About this task

Set up event filters before starting a Task Mining project you want the filter to apply to. To create or change an event filter during a project, workstation users must manually restart the Task Mining agent on their workstation.

Use a replacement filter to anonymize sensitive data for either the details of a native application or a specific page in any application.

-   Replace the details of a native application to prevent the Task Mining agent from collecting any information from a specific application while still collecting correct timestamps of activities. For example, you might not want to collect any data from workstation users working in a native app supporting payroll data.
-   Replace a page in any of its occurrences to prevent the Task Mining agent from collecting sensitive information from a specific page in any application. For example, you might not want to collect data from a personal payslip page through whatever browser workstation users use.

The Event Field Replacement Value anonymization value affects the output of this filter. For more information, see [Define Task Mining anonymization](define-anonymization.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Task Mining Workspace**.

2.  Select the Configuration icon ![](../image/task-mining-configuration-icon.png).

3.  Select **Event Filter**.

4.  Select **New**.

    **Note:** Not all fields on the Create New Event Filter form are required to create a replacement filter.

5.  In the **Filter Type** field, select **Replaced**.

6.  Create a Replaced filter for either the details of a native application or a page in all applications where the page occurs.

    |Option|Action|
    |------|------|
    |**Replace the details of a native application**|Enter the executable file name of the application in the **Application Name** field.|
    |**Replace a page in all applications where the page occurs**|Enter the window name in the **Window Name** field. To find the window name, hover over the window's tab in the web browser.|

7.  In the **Object Attribute** field, select all attributes in the raw data you want to replace.

    -   To replace URLs that can be exposed in the categorization process, select **URL**. Use this option in most situations. For example, you don't want to see personally identifiable information \(PII\) in Workday activity URLs, but you still want to categorize Workday activity.
    -   To prevent the Task Mining agent from collecting any sensitive or personally identifiable information and transferring it in the raw data, select **All**. This option still collects timestamps for the activities and displays the activity as BLOCKLISTED in analyses, but captures no details. For example, you might have regulatory or security requirements for anonymization.
    -   To replace the field names that can be transferred in the raw data, select **Name**. This option still collects details for the activities, but displays BLOCKLISTED in the data. Use this option when you have sensitive field names you don't want exposed in the data.
    -   To replace the value of fields that might contain PII that can be transferred in the raw data, select **Value**. This option still collects details for the activities, but displays BLOCKLISTED in the data. Use this option when you have fields containing sensitive data you don't want exposed in the data.
8.  Select **Save**.


