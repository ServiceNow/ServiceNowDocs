---
title: Enable the Create Case UI action for case type selection
description: Enable the Create Case UI action for case type selection for one or more selected tables.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Enable the Create Case UI action for case type selection

Enable the **Create Case** UI action for case type selection for one or more selected tables.

## Before you begin

Role required: workspace\_admin, ui\_builder\_admin, admin

## About this task

This procedure adds the **Create Case** UI action to records in the configured table. Selecting this UI action displays the Select a case type pop-up window .

**Note:** For the CSM Configurable Workspace, the **Create Case** UI action for case type selection is disabled out of box.

## Procedure

1.  Navigate to the Action Assignments list by entering **sys\_declarative\_action\_assignment\_list.do** in the application navigator.

2.  Filter the actions for the table on which you want the **Create Case** UI action to be enabled.

    For example, to enable the UI action for the Interaction table, use the **Table** column to filter for the Interaction \[interaction\] table.

3.  Select the **Create Case** action with this description:

    This Creates Case UI action enables the agent to create a case on Agent Workspace by selecting the type of case from a list of available case types.

4.  On the Create Case Action Assignment record, enable the **Active** check box and save the record.

5.  Navigate to the UI Actions list by entering **sys\_ui\_action\_list.do** in the application navigator.

6.  Filter the actions for the same table as selected in step 2.

7.  Select the **Create Case** action with no comments.

8.  On the Create Case UI Action record, disable the **Active** check box and save the record.

9.  Repeat steps 1 through 8 for each table on which you want to enable the **Create Case** UI action for case type selection.


