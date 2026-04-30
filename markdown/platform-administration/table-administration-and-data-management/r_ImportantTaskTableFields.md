---
title: Important Task table fields
description: The Task table is a base class that provides fields for the core ITSM applications such as Incident, Problem, and Change Management. All applications that extend the Task table share these fields in common.
locale: en-US
release: xanadu
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Task table structure, Working with the Task table, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Important Task table fields

The Task table is a base class that provides fields for the core ITSM applications such as Incident, Problem, and Change Management. All applications that extend the Task table share these fields in common.

<table id="table_phh_g11_tp"><thead><tr><th>

Label

</th><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

active

</td><td>

boolean

</td><td>

Specifies whether work is still being done on a task or whether the work for the task is complete. By default, only application-specific business rules set the value of this field. For example, the **incident autoclose** business rule closes resolved incidents that have not been updated for one day.

</td></tr><tr><td>

Additional comments

</td><td>

comments

</td><td>

journal\_input

</td><td>

Displays and allows the entry of comments about the task record. Each comment is inserted into the **Activity** field. For more information, see [Journal field type](../../field-administration/concept/c_JournalFields.md).

</td></tr><tr><td>

Approval History

</td><td>

approval\_history

</td><td>

journal

</td><td>

Displays the history of approvals for the record. For more information, see [Tools for completing tasks](../concept/c_TaskTable.md#section_mzc_z4g_3cc).

</td></tr><tr><td>

Assigned To

</td><td>

assigned\_to

</td><td>

reference

</td><td>

Specifies the user assigned to complete the task. By default, this field uses a [Reference qualifiers](../../../script/server-scripting/concept/c_ReferenceQualifiers.md) to only display users with the itil role.

 Some applications override the parent reference qualifier to display relevant users. For example, the Service Order and Project Task tables filter users based on their skills.

</td></tr><tr><td>

Created

</td><td>

sys\_created\_on

</td><td>

glide\_date\_time

</td><td>

Displays the date and time when the task record was created.

</td></tr><tr><td>

Description

</td><td>

description

</td><td>

string

</td><td>

Displays and allows the entry of a multi-line description of the work to be done.

</td></tr><tr><td>

Escalation

</td><td>

escalation

</td><td>

integer

</td><td>

Indicates how long the task has been open. Escalations are dynamically populated using service level agreements, which specify how long a task remains in each escalation state. Escalation states go from **Normal** to **Moderate** to **High**, and finally to **Overdue**. Record lists color code each task by escalation state.

</td></tr><tr><td>

Number

</td><td>

number

</td><td>

string

</td><td>

Displays an identifying number for each task record. This field is the display value for the Task table. The system generates this number when the task is created.

 To manage number generation, see [Record numbering](../../field-administration/concept/c_ManagingRecordNumbering.md).

</td></tr><tr><td>

Opened

</td><td>

opened\_at

</td><td>

glide\_date\_time

</td><td>

Displays the date and time when a human opened the task record for the first time.

</td></tr><tr><td>

Priority

</td><td>

priority

</td><td>

integer

</td><td>

Specifies how high a priority the task should be for the assignee. By default, the **calculatePriority**business rule calculates this value based on the **Impact** and **Urgency** values. Record lists color code each task by degree of priority.

</td></tr><tr><td>

Short Description

</td><td>

short\_description

</td><td>

String

</td><td>

Displays and allows the entry of a short description of the task, which is a human-readable title for the record.

</td></tr><tr><td>

State

</td><td>

state

</td><td>

Integer

</td><td>

Displays a choice list for status of the task:

-   Pending
-   Open
-   Work in Progress
-   Closed Complete
-   Closed Incomplete
-   Closed Skipped

 Applications typically use [Dictionary overrides](../../data-dictionary-tables/concept/c_DictionaryOverrides.md) to display application-specific states.

</td></tr><tr><td>

Sys ID

</td><td>

sys\_id

</td><td>

GUID

</td><td>

Displays the [Unique record identifier \(sys\_id\)](../../table-administration/concept/c_UniqueRecordIdentifier.md#).

</td></tr><tr><td>

Task Type

</td><td>

sys\_class\_name

</td><td>

sys\_class\_name

</td><td>

Specifies the type of task, which corresponds to the child class. The system populates this value when a record is created on a child table.

</td></tr><tr><td>

Time Worked

</td><td>

time\_worked

</td><td>

timer

</td><td>

Display a timer which measures how long a record is open in the form view.

</td></tr><tr><td>

Watch list

</td><td>

watch\_list

</td><td>

glide\_list

</td><td>

Specifies users who receive [Email and SMS notifications](../../notification/concept/c_EmailNotifications.md) when the record is updated. By default, only the Incident, Change, and Service Catalog applications notify users listed in this field. For other Task-based applications, you must create custom email notifications sent to the users listed in this field.

</td></tr><tr><td>

Work notes

</td><td>

work\_notes

</td><td>

journal\_input

</td><td>

Displays and allows the entry of comments viewable only by ITIL users. Each comment is inserted into the **Activity** field. For more information, see [Journal field type](../../field-administration/concept/c_JournalFields.md).

</td></tr><tr><td>

Work notes list

</td><td>

work\_notes\_list

</td><td>

glide\_list

</td><td>

Specifies users who receive [Email and SMS notifications](../../notification/concept/c_EmailNotifications.md) when work notes are added to the record. By default, only the Change, Problem, and Service Catalog applications notify users listed in this field. For other Task-based applications, you must create custom email notifications sent to the users listed in this field.

</td></tr></tbody>
</table>**Parent Topic:**[Task table structure](../../table-administration/concept/task-table-structure.md)

