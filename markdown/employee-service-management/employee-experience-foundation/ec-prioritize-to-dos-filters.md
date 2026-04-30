---
title: Enable prioritization by filter
description: If you are ordering the to-dos by filter instead of due date, you must enable the sn\_hr\_sp.todos\_config\_display\_with\_priority property, add the Display priority field to the to-dos configuration form, and assign each to-dos filter a priority number.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Employee tasks page, Setup task management and integration features, Configure, Employee Center, Employee Service Management]
---

# Enable prioritization by filter

If you are ordering the to-dos by filter instead of due date, you must enable the **sn\_hr\_sp.todos\_config\_display\_with\_priority** property, add the **Display priority** field to the to-dos configuration form, and assign each to-dos filter a priority number.

## Before you begin

Role required: sn\_hr\_sp.esc\_admin

The to-dos will then be sorted by the filter they are associated with. Within each filter, the to-dos will be sorted by due date.

When defining conditions like case sensitivity or null values, see API[GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

## Procedure

1.  Enable the **sn\_hr\_sp.todos\_config\_display\_with\_priority** property.

    1.  In the navigation filter, enter `sys_properties.list`.

        The System Properties list is displayed.

    2.  Open the **sn\_hr\_sp.todos\_config\_display\_with\_priority** property.

    3.  In the **Value** field, set the value to `true`.

2.  Add the **Display priority** field to the to-dos filter form.

    1.  Navigate to **Employee Center** &gt; **Administration** &gt; **To-dos Configuration**.

    2.  Or, navigate to **Employee Center Pro** &gt; **Administration** &gt; **To-dos Configuration**

    3.  Open a record.

    4.  In the to-dos configuration form header, click the menu icon and navigate to **Configure** &gt; **Form Layout**.

        **Note:** Ensure you are in the Employee Center Core application.

    5.  Move the **Display priority** field to the **Selected** column.

    6.  Click **Save**.

3.  Set the priority number for each to-dos filter.

    1.  Navigate to **Employee Center** &gt; **Administration** &gt; **To-dos Configuration**.

    2.  Open a to-dos filter record.

    3.  In the **Display priority** field, set the priority number.

    4.  Repeat the process for each filter.


