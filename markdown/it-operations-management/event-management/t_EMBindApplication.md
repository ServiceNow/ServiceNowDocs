---
title: Bind alerts to a specific process
description: Bind specific server processes to their corresponding Configuration Items \(CIs\) in the CMDB to ensure accurate mapping and visibility. This binding is crucial for identifying service dependencies, reducing ambiguity from generic process names, and enabling effective monitoring. It supports faster alert resolution, impact analysis, and better alignment between infrastructure and application components in dynamic environments.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Bind host CIs using CI field matching, Overriding default binding, Binding alerts to CIs, Event rules, Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Bind alerts to a specific process

Bind specific server processes to their corresponding Configuration Items \(CIs\) in the CMDB to ensure accurate mapping and visibility. This binding is crucial for identifying service dependencies, reducing ambiguity from generic process names, and enabling effective monitoring. It supports faster alert resolution, impact analysis, and better alignment between infrastructure and application components in dynamic environments.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

Sometimes, when an alert \(or event\) comes into the system, it needs to be connected — or "bound" — to a Configuration Item \(CI\) in the CMDB. By default, the system binds alerts to host specified in the **Node** field of the event. Imagine a situation where you have a Windows server running multiple processes, like MSFT SQL Instances and SQL Server Analysis Services. The challenge is to bind an event to the specific process instance rather than just the host server, as multiple processes could have the same generic name, such as MSSQLSERVER, leading to ambiguity.

The following example procedure uses a Windows server as the host, MSFT SQL Instances as the CI class of the process, and MSSQLSERVER as the process name. The following steps are based on the assumption that the event **Node** field of the event provides the host name, and the **Additional Information** field contains specific process details required for binding.

<table id="table_jpt_lts_2fc"><thead><tr><th>

Action

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Set event rule: Add process name

</td><td>

Add the process name `sa_process_name` in the event rule.

</td></tr><tr><td>

Set event rule: Define CI type

</td><td>

Select the target CI type in the event rule. For example, MSFT SQL Instances.

</td></tr><tr><td>

Define process mapping

</td><td>

Navigate to the Process to CI Type Mapping table \[em\_binding\_process\_map\] and add an entry mapping a CI type \(e.g., MSFT SQL Instances\) to a process name \(e.g., MSSQLSERVER\).

</td></tr><tr><td>

Bind CI to alert

</td><td>

When an event is triggered, the system:1.  Applies default binding to identify the host.
2.  Checks the CI type specified in the event rule.
3.  Looks up the Process to CI Type Mappings table \[em\_binding\_process\_map\] for a matching process name and CI type.
4.  Searches the CI Relationships table \[cmdb\_rel\_ci.list\] for a Runs on::Runs relationship between the process and the host CI.
5.  Binds to a process when values from the **CI Type** column match the corresponding entries in the **Process** column in the Process to CI Type Mappings table \[em\_binding\_process\_map\].

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Event Rules**.

2.  Select **New**.

3.  Select the **Transform and Compose Alert Output** tab and perform the following steps:

    ![Add sa_process_name.](../image/em-sa-process-name.png)

    1.  Select the **Manual attributes** check box.
    2.  Enter `sa_process_name` is `${process}`.

        sa\_process\_name is a special variable name used to specify the name of the process to search for. $\{sa\_process\_name\} will appear in the **Additional information** field of the event. Instead of `${process}`, you can enter any other field name from which the variable `sa_process_name` derives its value.

4.  Select the **Binding** tab.

5.  Select the **Override default binding** check box.

6.  In the **Binding type** field, select **CI field matching**.

7.  In the **CI type** field, select **MSFT SQL Instances**.

    The **CI type** determines the specific CMDB table where the system searches for the matching CI.

    ![Add CI type.](../image/em-binding-ci-type.png)

8.  Navigate to **All** and search `em_binding_process_map.list`.

    The Process to CI Type Mappings page opens. Here the values from the **CI type** column are mapped to entries in the **Process** column. For example, **cmdb\_ci\_db\_mssql\_instance** is mapped to the **MSSQLSERVER** process.

    ![The CI type values are matched with the corresponding entries in the Process column.](../image/em-processing-map.png)

9.  Navigate to **All** and search `cmdb_rel_ci.list`.

    The CI Relationships page opens.

10. Verify that the node is in a Runs on::Runs relationship with the appropriate process.

    ![The node linked to the appropriate process via a Runs on::Runs relationship.](../image/em-verify-runs-relationship.png)

11. Navigate to **All** &gt; **Event Management** &gt; **All Events**.

12. Create an event with **Node** value as the name of the host such as Windows Server \(V-W2K3-SQL2008\).

    The **Additional information** field in the event has a key called **process** whose value is **MSSQLSERVER**.

    In the following image, you can see the processing notes indicating that the binding has occurred between the alert and the matching process.

    ![Processing notes confirming alert-process binding.](../image/em-processing-notes.png)


