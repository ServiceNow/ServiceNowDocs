---
title: Create a bulk case request using Agent Workspace for HR Case Management
description: Create bulk case requests through Agent Workspace for HR Case Management to create the same type of HR case for multiple employees without having to create the same case multiple times.
locale: en-US
release: australia
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Agent Workspace for HR Case Management, Agent Workspace, HR Service Delivery, Employee Service Management]
---

# Create a bulk case request using Agent Workspace for HR Case Management

Create bulk case requests through Agent Workspace for HR Case Management to create the same type of HR case for multiple employees without having to create the same case multiple times.

## Before you begin

Role required: sn\_hr\_core\_admin

## Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **Agent Workspace for HR Case Management**.

2.  Select the **Lists** icon \(![Lists icon](../image/agent-ws-hr-list-icon.png)\).

3.  Navigate to **Bulk cases** &gt; **Bulk case requests**.

4.  Select **New**.

5.  On the form, fill in the fields.

    For more information, see [Bulk case request form](../reference/bulk-case-request-form.md).

6.  Select **Save**.

    The **Details**, **User segment groups** and **Cases created** tabs are displayed.

7.  Create a user segment group.

    For more information, see [Specify a user segment group for a bulk case request in Agent Workspace for HR Case Management](segment-group-aws.md).

    **Note:** You can also configure fields that you want to view in the User segment group form by configuring fields in the Case Creation Configuration form. Navigate to **All** &gt; **HR Administration** &gt; **Case Creation Configuration**.

8.  View details of your bulk case request by selecting the **Details** tab when your segment status changes to **Processed**.

9.  Create cases for all users with a status of Included who meet the filter criteria by selecting Create cases.

    **Note:** After selecting the **Create cases** button, all users with a status of **Included** are rechecked against the filter criteria used. Cases aren’t created for users that no longer match the filter criteria. Cases are also not created for users that match the criteria after the user segment was created.

10. Select the **Cases created** tab to view a list of cases created.


