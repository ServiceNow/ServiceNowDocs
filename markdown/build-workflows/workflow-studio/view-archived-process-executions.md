---
title: View archived process contexts
description: Configure the form layout for a process execution so that you can see the JSON record for archived context records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/view-archived-process-executions.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Archive process contexts, Administering Playbooks, Configure, Playbooks, Workflow Studio, Build workflows]
---

# View archived process contexts

Configure the form layout for a process execution so that you can see the JSON record for archived context records.

## Before you begin

Role required: admin or playbook.admin

## About this task

To view the archived context records for a process execution record, you must configure the Form Layout for process execution records. If you haven't archived any context records for a process execution and want to, see [Archive process contexts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/archive-process-executions.md).

## Procedure

1.  Navigate to **All**, and enter **sys\_pd\_context.list** in the Filter field to open the \[sys\_pd\_context\] table.

2.  Open any process execution.

3.  Open the form context menu \(\[Omitted image "ContextMenu.png"\] Alt text: Context menu icon\).

4.  Select **Configure** &gt; **Form Layout**.

5.  In the Available list, double-click **Archive** to move it to the **Selected** list.

    \[Omitted image "config-exe-form-layout.png"\] Alt text: Configuring the form layout to show the Archive field in process execution records

6.  Select **Save**.

    The Archive field appears in all process execution records.

7.  Open a process execution with archived process context records.

    You can view the JSON record of the archived context records for the process execution in the Archive field.


## Add the Archive field to the form

\[Omitted image "view-archived-json.gif"\] Alt text: Adding the Archive field to the form layout

**Parent Topic:**[Archive process contexts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/archive-process-executions.md)

