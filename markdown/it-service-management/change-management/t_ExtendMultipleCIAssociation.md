---
title: Extend or disable multiple CI association
description: The ability to associate multiple CIs to a task can be extended to other types of tasks. You can also disable multiple CI association from the related lists on change request records.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure, Change Management, IT Service Management]
---

# Extend or disable multiple CI association

The ability to associate multiple CIs to a task can be extended to other types of tasks. You can also disable multiple CI association from the related lists on change request records.

## Before you begin

Role required: admin

## Procedure

1.  In the navigation filter, enter `sys_properties.list` to open the System Property \[sys\_properties\] table.

2.  Open the **List of all the task types where user wants to associate CIs using a List** \(**com.snc.task.associate\_ci**\) system property.

    The value of this property is set to change\_request, incident by default to enable association of multiple CIs to change requests.

3.  To enable multiple CI association to other types of task, add the required table as a value.

    For example, to enable multiple CI association for problem records, add `problem` as a value, separated by a comma.

4.  Click **Update** to save and update the property.

5.  Complete the following steps to disable multiple CI association for the Change Request form.

    1.  Remove the **change\_request** value from the **List of all the task types where user wants to associate CIs using a List** \(**com.snc.task.associate\_ci**\) system property.

    2.  Navigate to **System UI** &gt; **List control**.

    3.  Perform one or both of the following tasks to disable multiple CI association for the related lists.

<table id="table_s5v_3z3_11b"><tbody><tr><td>

**Associated CIs**

</td><td>

Open the entry with the **task\_ci.task** related list and clear the **Omit edit** check box.

</td></tr><tr><td>

**Impacted Services/CIs**

</td><td>

Open the entry with the **task\_cmdb\_ci\_service.task** related list and clear the **Omit edit** check box.

</td></tr></tbody>
</table>
**Parent Topic:**[Configuring Change Management](../concept/configure-change-management.md)

