---
title: Delete a field from a table
description: You can delete custom fields that you created. Custom fields begin with u\_. It is recommended that you remove the field from forms and lists instead of deleting it.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Add and customize a field in a table, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Delete a field from a table

You can delete custom fields that you created. Custom fields begin with **u\_**. It is recommended that you remove the field from forms and lists instead of deleting it.

## Before you begin

Role required: admin

## About this task

You cannot delete base system fields. In addition, any missing base system fields are recreated when the instance is upgraded.

## Procedure

1.  Navigate to a form that contains a custom field to delete.

2.  Right-click the field label and select **Configure Dictionary**.

3.  Click **Delete Column** in the form header, and then click **OK**.

4.  To delete multiple custom fields, complete the following steps.

    1.  Navigate to **System Definition** &gt; **Dictionary**.

    2.  Locate the custom fields to delete.

        For example, search for column names that start with `u_`.

    3.  Check the boxes next to the fields to delete and select **Delete** from the action list below the list.

        A confirmation dialog opens and reminds you that this may result in deletion of related records. If there are dependencies for the selected fields, they are listed.

    4.  To proceed, click **Delete**.


**Parent Topic:**[Add and customize a field in a table](../../field-administration/task/t_CreatingNewFields.md)

