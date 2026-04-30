---
title: Specify a default field value
description: A default value populates a value in a field when a new record is created.Review the following examples about specifying default field values.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Customizing fields, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Specify a default field value

A default value populates a value in a field when a new record is created.

## Before you begin

Role required: personalize\_dictionary

## About this task

The default value populates the field on the blank form for a new record, and also subsequently when the new record is submitted if the field is empty. Default values can be specified as either a constant or generated through script.

## Procedure

1.  Right-click the field's label in the form and select **Configure Dictionary**.

2.  Enter the default value in the **Default value** field.

    To set a constant value, type it into the **Default value** text box field. To assign a default value using a more complex formula, use JavaScript to output a default value.

    **Note:** The default value should be the underlying value that would be present in the field, not the label. For example, in a choice list field, use the **value** of the choice as the default value, not the choice's name.


**Parent Topic:**[Customizing fields on the ServiceNow AI Platform](../concept/customize-fields-now-platform-landing.md)

## Default field value examples

Review the following examples about specifying default field values.

### Constant default values

Here is an example that sets a default value for the **Priority** field.

![](../image/DefaultValueConstant.png "Default value constant")

### Javascript default values

To view out-of-box examples of JavaScript default values, navigate to **System Definition** &gt; **Dictionary** and enter this filter: **\[Default value\] \[starts with\] \[javascript\]**. Open some of the records and view the default value javascript entries.

### Set a default value for assignment\_group

The following example sets a default value in a \[sys\_user\_group\] reference field by getting the ID from the name of a group.

```
javascript:GetIDValue('sys_user_group', 'Development');
```

### Set a default value for assigned\_to if user has the itil role

This example for the Task \[task\] table describes how to configure the default value for the \[assigned\_to\] user equal to the current user id if the user has a role of itil.

-   Column label: **Assigned to**
-   Column name: **\[assigned\_to\]**
-   Reference Specification section
    -   Reference: **User** \[sys\_user\]
    -   Reference qual condition: **\[Roles\] \[is\] \[itil\]**
-   Default value script:

    ```
    javascript:if (gs.hasRole("itil"))current.assigned_to = gs.getUserID();
    ```


### Set a default value for a duration field

To set a default value for a duration field, use the following in the **Default value** field of the duration field's dictionary entry:

```
javascript:current.duration_field.setDisplayValue('3 04:30:14');
```

Avoid hard-coding a particular date-time. If the system date-time format changes, the value becomes invalid. Instead, select the **Use dynamic default** check box and assign a dynamic filter option. For more information on dynamic filters, see [Create a dynamic filter option](https://www.servicenow.com/docs/access?context=t_DynamicFilterOptions&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) .

