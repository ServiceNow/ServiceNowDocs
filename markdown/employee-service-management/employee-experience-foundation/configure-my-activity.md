---
title: Perform an advanced activity configuration
description: Configure activities to display their count and to display items in a list for a primary activity.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [My active items widget configuration, Setup task management and integration features, Configure, Employee Center, Employee Service Management]
---

# Perform an advanced activity configuration

Configure activities to display their count and to display items in a list for a primary activity.

## Before you begin

Role required: admin, sp\_admin, or ESC admin

## Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **Activity Configuration**.

2.  Click **New**.

3.  On the form, fill in the fields.

    For more information about the form fields and descriptions, see [Activity Configuration form](../reference/ec-activity-configuration-form.md).

4.  Select the **Advanced** option.

5.  In the **Summary view script** field, add a script to display the count of activities, for example, `new sn_ex_sp.ActivityConfigurationUtil().getTasksCount();`

    The API returns an integer value.

6.  In the **List View script** field, add a script to display items in a list, for example, `new sn_ex_sp.ActivityConfigurationUtil().getMyTodos(recordsLimit);`

    **Note:** Do this step only if you have marked this activity as primary by selecting the **primary** option.

7.  On **List view json**, provide a template with mapping of table fields to component properties.

    For example, `{ 'badge': '', 'badgeColor': '', 'image': '', 'title': '', 'description': '', 'field1Label': '', 'field1Value': '', 'field2Label': '', 'field2Value': '', 'itemUrl': '', 'target': '' // target is '' if its internal or portal page url. target is '_blank' if url is external }`

8.  Click **Save** or **Submit**.


## What to do next

If you click **Save**, the **Activity Access** tab appears. For more information, see [Restrict access to an activity](grant-restrict-activity-access.md).

