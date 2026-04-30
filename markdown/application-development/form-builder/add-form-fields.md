---
title: Add fields to a form layout in Table Builder
description: Visually add and arrange fields within a form layout to create a form that matches your requirements using Table Builder.
locale: en-US
release: yokohama
product: Form Builder
classification: form-builder
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Forms in Table Builder, Using Table Builder, Table Builder, Builder library, Developing your application, Building applications]
---

# Add fields to a form layout in Table Builder

Visually add and arrange fields within a form layout to create a form that matches your requirements using Table Builder.

## Before you begin

-   Launch Table Builder. For more information, see [Accessing Table Builder](../concept/accessing-form-builder.md).
-   \(Optional\) Choose a domain to work within \(if not global\). For more information, see [Domain separation and Table Builder](../concept/form-builder-domain-separation.md).
-   \(Optional\) Choose an application scope to work within \(if not global\). For more information, see [Using an application scope with Table Builder](../concept/fb-application-scope.md).

**Note:** To understand how to approach customizing your forms, review [Table Builder workflow and navigation](../concept/form-builder-workflow.md).

Role required: personalize\_form or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

## About this task

## Procedure

1.  Navigate to the **Forms** tab in Table Builder.

2.  Choose a view to work with.

    For detailed information on how to choose a view for a form, see [Choose a form view in Table Builder](manage-form-views.md).

3.  To display a list of the existing fields for the selected table, in the add form elements panel, select **Fields**.

    **Note:** You can also launch the Add form elements panel by selecting the Add \(![Add icon.](../image/fb-add-icon.png)\) icon above any existing element in the form editor.

4.  Customize the fields that display on the selected form view by performing one of the following actions.

    **Note:** Certain field types are only supported in Core UI. Fields are flagged with an exclamation icon \(!\) to indicate an unsupported type.

<table id="choicetable_u3j_f4j_wrb"><thead><tr><th align="left" id="d254300e200">

Option

</th><th align="left" id="d254300e203">

Action

</th></tr></thead><tbody><tr><td id="d254300e209">

**Add an existing field to a form**

</td><td>

1.  To select a field, click a field in the list.

**Note:** To select multiple fields, select the option that displays on the right of the field.

2.  In the form editor, drag one or more selected fields to the desired location and then move them around as necessary.


</td></tr><tr><td id="d254300e229">

**Add a new field to a form**

</td><td>

1.  Select **+ Add a field in the table**.
2.  In the **Column Label** field, enter a label.
3.  In the **Column name** field, enter the internal name for the field.
4.  Select the type of field from the **Type** list.

To set additional properties for the field that you are creating, click **Advanced settings**. For information on field types and advanced settings, see [Field configuration in Table Builder](../reference/field-parameters.md).

5.  To add the new field to the table, click **Add**.

A confirmation dialog displays. You can click **Done** to close it or click **Add another one** to add more fields to the table.

The new field is displayed at the top of the Fields list and can be dragged onto the form editor.

</td></tr><tr><td id="d254300e295">

**Remove field from form**

</td><td>

1.  In the form editor, click a field to select it.
2.  To remove the selected field from the form view, click the x icon to the right of the field.
 **Note:** If you are unable to delete a field, it may be because the table belongs to a different scope.

</td></tr></tbody>
</table>5.  Select **Save**.


**Parent Topic:**[Forms in Table Builder](../concept/form-view-configuration.md)

