---
title: Create a case in Agent Workspace for HR Case Management
description: Create a new HR case in Agent Workspace for HR Case Management.
locale: en-US
release: zurich
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Agent Workspace, HR Service Delivery, Employee Service Management]
---

# Create a case in Agent Workspace for HR Case Management

Create a new HR case in Agent Workspace for HR Case Management.

## Before you begin

Role required: sn\_hr\_core.case\_writer

## Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **Agent Workspace for HR Case Management**.

2.  To create an HR case, select the **Add** icon \(plus sign\).

3.  In the search field, enter a name, partial name, or case number.

    Searching for an employee helps to verify that you are creating a case for the correct person.

    **Note:**

    -   You can search for or create cases for inactive users in Agent Workspace for HR Case Management.
    -   If your company uses **Employee Relations**, you can select the **Skip verification** link to create an ER case without identifying an Opened for person. For more information on Employee Relations, see [Create an Employee Relations case in Core UI](create-hr-employee-relations.md).
4.  Select **Next**.

5.  On the form, fill in the fields.

    For more information, see [Create a new case form](../reference/case-creation-form-aws.md).

6.  Select **Create case**.

    If the case being created has the same subject person, HR service, and if the case is created within three days \(configurable from HR Administration/Properties\), a warning appears that a similar case might already exist. You can choose to **Create new case** or **Cancel**.

    **Note:** For information on the sn\_hr\_core.duplicate\_hr\_case\_time\_out property, see [HR properties](t_HRProperties.md).


