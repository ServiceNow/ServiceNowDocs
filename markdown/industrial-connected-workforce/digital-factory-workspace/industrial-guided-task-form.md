---
title: Industrial Guided Task form
description: The following table describes the field values for the Industrial Guided Task form.
locale: en-US
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Industrial Guided Tasks, Reference, Digital Factory Workspace, Industrial Connected Workforce]
---

# Industrial Guided Task form

The following table describes the field values for the Industrial Guided Task form.

<table id="table_aj2_g4n_c2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique number for the task.

</td></tr><tr><td>

Priority

</td><td>

Options are:-   1 - Direct
-   2 - This shift
-   3 - Today
-   4 - Within 7 days
-   5 - Within 30 days
-   6 - Unplanned

</td></tr><tr><td>

Short description

</td><td>

Auto-populated with the name of the standard from which the task is being created.

</td></tr><tr><td>

Work notes

</td><td>

Additional information and comments that can help execute the task successfully.

</td></tr><tr><td>

Assignment group

</td><td>

Group of users that the task can be assigned to.

</td></tr><tr><td>

Assigned to

</td><td>

User that the task has been assigned to.

</td></tr><tr><td>

Functional location

</td><td>

Industrial facility work area where the task is to be completed. Defined using the ISA-95 standard as an operational model site. Automatically filled based on the logged-in user's worker profile.

</td></tr><tr><td>

Equipment

</td><td>

Machine to which the task relates. This field is already populated if the equipment is specified in the standard.

</td></tr><tr><td>

Planned start

</td><td>

Planned start of the task execution.

</td></tr><tr><td>

Planned end

</td><td>

Planned end of the task execution.**Note:** If you create a task without a planned end date, the system automatically sets the planned end to match the due date. This automatic population enables the embedded dashboard to use the planned end data for calculations, such as measuring the percentage of tasks closed in time.

</td></tr><tr><td>

Due date

</td><td>

The date by which the task is to be executed. If not set, it’s calculated based on priority. For more details, see [Due date calculation](due-date-calculation.md).

</td></tr></tbody>
</table>**Parent Topic:**[Industrial Guided Tasks reference](industrial-guided-tasks-reference.md)

