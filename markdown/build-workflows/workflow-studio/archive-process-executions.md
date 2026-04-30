---
title: Archive process contexts
description: Improve database query performance by archiving unneeded records for playbooks that are in a Complete, Error, or Cancelled state.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Administering playbooks, Configuring playbooks, Configuring Workflow Studio, Workflow Studio, Build workflows]
---

# Archive process contexts

Improve database query performance by archiving unneeded records for playbooks that are in a **Complete**, **Error**, or **Cancelled** state.

## Before you begin

Role required: admin or playbook.admin

## About this task

Depending on how many playbooks you have run, you may have hundreds or thousands of records in your database that aren't used anymore. Reduce the number of records that your database queries have to search through by archiving the records for playbooks that are in a **Complete**, **Error**, or **Cancelled** state.

By default, context records are automatically archived for process executions that are:

-   In **Complete**, **Skipped**, or **Cancelled** state
-   For a playbook that hasn’t been edited within 14 days.

    **Note:** You can adjust the number of days. To learn more about configuring archive settings, see [Configure archive settings for process contexts](config-archive-settings-process-contexts.md).


If you don't want context records to automatically be archived, see [Turn off automated archiving](turn-off-automated-archiving.md).

Contexts for process executions that are in an **Error** state must be archived manually.

**Note:** If you no longer need logs for a process execution that ended in an error, archive the context records.

When you archive context records for a process execution, the following records are compressed into a single JSON record:

-   Element mapping \[`sys_element_mapping`\]
-   Context log \[`sys_pd_context_logs`\]
-   Variable value \[`sys_variable_value`\]
-   Activity context \[`sys_pd_activity_context`\]
-   Stage context \[`sys_pd_lane_context`\]

The JSON record can be viewed, but not edited. To learn more about viewing the JSON record for archived context data, see [View archived process contexts](view-archived-process-executions.md).

**Warning:** Archiving cannot be undone. If you need context logs or reports that use these records, don’t archive. If automated archiving creates report problems, turn off the feature. To learn how to turn off automated archiving, see [Turn off automated archiving](turn-off-automated-archiving.md).

Agents can still open playbooks to see historical data, such as why a playbook was canceled or who an activity was assigned to.

Flow context \(`sys_flow_context`\) records are also deleted automatically 2 weeks after completion. For more information about flow data retention, see [Flow execution details retention](../../flow-designer/concept/flow-reporting.md).

## Procedure

1.  Manually archive context records for a process execution
2.  Navigate to **All**, and enter **sys\_pd\_context.list** in the Filter field to open the \[sys\_pd\_context\] table.

3.  Select the check boxes next to the executions that you want to archive context records for.

4.  In the upper right corner, select **Archive Process Contexts** from the action menu.

5.  Confirm that you want to archive the process contexts.


## Result

The context records are archived for your selected process executions.

If you have a large number of context records to archive, records are archived in limited batches on an hourly basis, to avoid slowing down the instance.

## Archive context records for an execution

![Archive context records for a process execution](../images/archive-process-context.gif)

## What to do next

Configure the form layout for process executions so that you can see the archived data. To learn more about configuring the form layout for a process execution, see [View archived process contexts](view-archived-process-executions.md).

-   **[Configure archive settings for process contexts](config-archive-settings-process-contexts.md)**  
Change the default settings for the automated archiving feature for process contexts.
-   **[Turn off automated archiving](turn-off-automated-archiving.md)**  
Turn off the automatic archiving of context records for your complete and cancelled playbooks.
-   **[View archived process contexts](view-archived-process-executions.md)**  
Configure the form layout for a process execution so that you can see the JSON record for archived context records.

**Parent Topic:**[Administering playbooks](../concept/administering-process-automation-designer.md)

