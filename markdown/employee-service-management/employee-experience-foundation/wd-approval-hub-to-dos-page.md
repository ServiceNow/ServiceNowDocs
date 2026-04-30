---
title: Use task configuration for Workday approvals
description: Using the default To-dos configuration, you can provide the approvers with more in-context information about the approval requests for better approval workflows.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Approvals hub integration with Workday, Approval hub integrations, Approvals hub, Setup task management, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Use task configuration for Workday approvals

Using the default To-dos configuration, you can provide the approvers with more in-context information about the approval requests for better approval workflows.

## Before you begin

To-dos configurations are based on **Pulled Integration To-do** table and show **Open** and **Completed** approvals on **My tasks**. For more information on task configuration, see [Enable task configuration for approvals](approval-hub-to-dos-page-filters.md)

Role required: sn\_hr\_sp.esc\_admin

## Procedure

1.  Go to **All** &gt; **Employee Center** &gt; **Administration** &gt; **To-dos Configuration**, click an existing to-dos configuration, and navigate to the **Task Configuration** related list.

2.  Click **New** or edit an existing task configuration record such as **workday**.

3.  Understand the configuration as explained in [Enable task configuration for approvals](approval-hub-to-dos-page-filters.md) for more contextual info about the request.

4.  Use the default configuration or modify per your business requirements.

    Table name configured in the to-dos configuration to which the task config is associated **Pulled Integration To-do \[sn\_hr\_integr\_fw\_todo\_inbound\]**.

5.  Use the default tab configuration or modify to suit your requirements.

    -   The **Details** tab shows all the additional information about the request.
    -   The **Comments** tab shows all comments about the request.
    -   The **Attachments** tab shows all attachments about the request.
6.  Click **Actions** to search and select the required action group.

    Select the actions to display the frequently used actions such as **Approve** or **Reject**. For more information, see [Action framework](../concept/action-group-framework.md).

7.  Click **Submit** or **Update**.


## Result

Based on this configuration, the approvers see the in-context information about the Workday approval and process the approval. For more reference info, see [Approvals experience reference](../reference/approval-hub-ootb.md).

## What to do next

Based on the configuration, the approver can see information and process the approvals. For more information, see [Use Approvals hub](ec-to-dos-use-approval-hub.md).

**Parent Topic:**[Approvals hub integration with Workday](../concept/wd-ec-integration.md)

