---
title: Extend or disable multiple CI association
description: Extend multiple CI association to other task types, or disable it for change requests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/t\_ExtendMultipleCIAssociation.html
release: brazil
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure, Change Management, IT Service Management]
---

# Extend or disable multiple CI association

Extend multiple CI association to other task types, or disable it for change requests.

## Before you begin

Role required: admin

## Procedure

1.  In the navigation filter, enter `sys_properties.list` to open the System Property \[sys\_properties\] table.

2.  Open the **List of all the task types where user wants to associate CIs using a List** \(**com.snc.task.associate\_ci**\) system property.

    The value of this property is set to change\_request, incident by default to enable association of multiple CIs to change requests.

3.  To enable multiple CI association to other types of task, add the required table as a value.

    For example, to enable multiple CI association for problem records, add `problem` as a value, separated by a comma.

4.  **Update** to save and update the property.

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
**Parent Topic:**[Configuring Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/configure-change-management.md)

