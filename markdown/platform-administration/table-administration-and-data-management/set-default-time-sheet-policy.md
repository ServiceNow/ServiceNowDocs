---
title: Set a time sheet policy as default policy
description: As a time card administrator, you can set a time sheet policy as the default policy. The default policy is a global time sheet policy which applies to all the users who are not assigned to any other time sheet policy.
locale: en-US
release: yokohama
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Time sheet policies, Time Card management, Work with the Task table, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Set a time sheet policy as default policy

As a time card administrator, you can set a time sheet policy as the default policy. The default policy is a global time sheet policy which applies to all the users who are not assigned to any other time sheet policy.

## Before you begin

Role required: timecard\_admin

## About this task

Only one time sheet policy can be set as a default policy.

## Procedure

1.  Navigate to **All** &gt; **Time Sheets** &gt; **Administration** &gt; **Time Sheet Policies**.

2.  Open the time sheet policy record.

3.  Click the **Set as default** related link.

    **Note:** The related link appears only for a time sheet policy which is not already set as the default policy.


## Result

The **Default Policy** option on the [record form](create-time-sheet-policy.md#time_sheet_policy_form) is selected to indicate that the current time sheet policy is set as the default policy. The **Default Policy** option on the earlier default time sheet policy is cleared.

You cannot delete a default time sheet policy. You must first mark another policy as the default policy to delete the current default policy.

**Parent Topic:**[Time sheet policies](../concept/time-sheet-policies.md)

