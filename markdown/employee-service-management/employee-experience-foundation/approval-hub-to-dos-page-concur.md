---
title: Use task configuration for SAP Concur approvals
description: Using the default To-dos configuration, you can provide the approvers with more in-context information about the approval requests for better approval workflows.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Approvals hub integration with SAP Concur, Approval hub integrations, Approvals hub, Setup task management, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Use task configuration for SAP Concur approvals

Using the default To-dos configuration, you can provide the approvers with more in-context information about the approval requests for better approval workflows.

## Before you begin

The following **To-dos Configurations** \(sn\_hr\_sp\_todos\_config\) are available by default.

-   Concur Expense Report - Approval
-   Concur Expense Report - Completed

To-dos configurations are based on **Pulled Integration To-do** table and show Open and Completed concur approvals on My tasks. For more information on task configuration, see [Enable task configuration for approvals](approval-hub-to-dos-page-filters.md)

Role required: sn\_hr\_sp.esc\_admin

## Procedure

1.  Go to **All** &gt; **Employee Center** &gt; **Administration** &gt; **To-dos Configuration**, click an existing to-dos configuration, and navigate to the **Task Configuration** related list.

2.  Click **New** or edit an existing task configuration record such as **Approval \| SAP Concur**.

3.  Understand the configuration as explained in [Enable task configuration for approvals](approval-hub-to-dos-page-filters.md)

4.  Use the default configuration or modify per your business requirements.

    -   Use the condition builder to specify the conditions that a task must meet to appear on the to-dos page. For example, Todo state is **open**, Source table is **sn\_ex\_cnc\_concur\_report**, and Active is **true** and so on.
    -   Table name configured in the to-dos configuration to which the task config is associated **Pulled Integration To-do \[sn\_hr\_integr\_fw\_todo\_inbound\]**.
    -   Reference table is **Concur Expense Report** \[sn\_ex\_cnc\_concur\_report\].
    -   Use the \{reference\_table.name\},\{reference\_table.report\_created\_date\},\{reference\_table.approval\_status\_name\} fields to display the table name, created date, and status.
    -   Ensure you configure the widget parameters to suit your requirements. For example, set the **showItemizations** and **showAttachments** value to **true** to show attachments and itemizations. When **showReportTotals** is true, the report shows the sum total of all the expenses.
5.  Use the default tab configuration **Expenses** and **Comments**or modify to suit your requirements.

    -   The **Expenses** tab shows all expenses for Concur report. Widget is **Concur Expenses** and **Concur Expenses Mobile**. You can see Itemizations and receipts.
    -   The **Comments** tab shows all comments for Concur report. Widget is **Concur Comments**.
6.  Click **Actions** to search and select the required action group.

    Select the **Concur actions** to display the frequently used actions such as **Approve**, **View receipts**, and **Send back**. For more information, see [Action framework](../concept/action-group-framework.md).

7.  Click **Submit** or **Update**.


## Result

Based on this configuration, the approvers see the in-context information about the Concur approval and process the approval. For more reference info, see [Approvals experience reference](../reference/approval-hub-ootb.md).

## What to do next

Approver users can see information and process the approvals. For more information, see [Use Approvals hub](ec-to-dos-use-approval-hub.md)

**Parent Topic:**[Approvals hub integration with SAP Concur](../concept/x-concur-sa-integration.md)

