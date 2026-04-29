---
title: Components installed with Retail Playbook for Store Plan
description: Certain roles and dependencies must be considered when using the Retail Playbook for Store Plan.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Components installed with plugins, Reference, Retail]
---

# Components installed with Retail Playbook for Store Plan

Certain roles and dependencies must be considered when using the Retail Playbook for Store Plan.

## Plugins installed with Retail Playbook for Store Plan

<table id="table_hyv_3yz_m3c"><thead><tr><th>

Plugin Name

</th><th>

Description

</th><th>

Plugin Dependencies

</th></tr></thead><tbody><tr><td>

Retail Playbook for Store Plan

 \[com.sn\_rtl\_str\_plan\_pb\] 

</td><td>

The Retail playbook for store plan enables HQ and regional managers to easily create structured operational plans with tasks and cases, linked to store locations and schedules.

</td><td>

-   com.sn\_retail\_core
-   com.sn\_csm\_playbook
-   com.sn\_tsk\_plan\_pb\_act
-   com.sn\_pwm\_pb\_act
-   com.sn\_rtl\_hq\_ops

</td></tr></tbody>
</table>## Activities associated with Retail Playbook for Store Plan

<table id="table_kyv_3yz_m3c"><thead><tr><th>

Activity Name

</th><th>

Activity Description

</th></tr></thead><tbody><tr><td>

Create Template item

</td><td>

Allows to create only one record through this activity. Displays a form based on the table and form view configured in the corresponding template item configuration, and creates the corresponding template item record.

 The form runs any UI policies that apply. The system displays any validation error messages in the Workspace playbook.

</td></tr><tr><td>

Create template items

</td><td>

Allows to create only multiple records through this activity. Displays the form based on the table and form view configured in the corresponding template item configuration, and creates the corresponding template item records.

 The form runs any UI policies that apply. The system displays any validation error messages in the Workspace playbook.

</td></tr><tr><td>

Select multiple records

</td><td>

Specify the template item to attach multiple records and activity experience configurations to render modal for record selection and insertion into an m2m table.

</td></tr><tr><td>

PWM Schedule

</td><td>

Allows creation of a schedule for task creation using a task plan template through the PWM scheduler.

</td></tr><tr><td>

Plan Summary

</td><td>

A summary view of the all activities configured in a playbook together for users to be able to edit before they publish the plan

</td></tr></tbody>
</table>## Retail Playbook for Store Plan details

|Playbook|Description|
|--------|-----------|
|HQ communication|Allows to create a plan with cases and tasks for multiples stores by a HQ/Regional manager.|

**Parent Topic:**[Components installed with plugins](rahi-retail-components-installed-with-plugins.md)

