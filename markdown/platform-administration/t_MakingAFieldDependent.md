---
title: Make a field dependent
description: A choice or reference field can be declared dependent on another field on the same table to limit the values available to select based on the value of the dependent field.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Customize, Field administration, Forms, fields, and lists, Configure core features, Administer]
---

# Make a field dependent

A choice or reference field can be declared dependent on another field on the same table to limit the values available to select based on the value of the dependent field.

## Before you begin

Role required: personalize\_dictionary or admin

## About this task

If a required dependency does not function as expected, as might happen if there is a many-to-many relationship between the fields, consider using reference qualifiers to accomplish the goal.

**Note:**

-   Fields cannot be made dependent on derived fields.
-   When you create a dependency between reference fields \(similar to assignment group and assigned to\), you must add `_group` to the name of the field on which the other is dependent on to get the expected behavior. See [KB0998861: Dependent field does not work as expected on task "Assigned to" field](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0998861) for more information.

## Procedure

1.  Navigate to a form that contains the field that you want to make dependent on another field.

    For example, to configure a field in the Incident \[incident\] table, navigate to **All** &gt; **Incident** &gt; **All** and select **New**.

2.  Right-click the field label in the form and select **Configure** &gt; **Dictionary**.

3.  From the Dependent field tab, select **Use dependent field** and select the name of the field that this field will depend on.

    **Note:** For some field types, you may only need to enter the name of a field in the same table on which the field depends.

4.  Select **Update**.


## Dependent field

In the example below, the Subcategory field is made dependent upon the Category field. On an incident form, the value selected for the Category field determines which options appear for the Subcategory field.

![Dependent Value](../image/DependentValue.png)

**Parent Topic:**[Customizing fields on the ServiceNow AI Platform](../concept/customize-fields-now-platform-landing.md)

**Related topics**  


[Reference qualifiers](../../../script/server-scripting/concept/c_ReferenceQualifiers.md)

