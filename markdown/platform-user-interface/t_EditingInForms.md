---
title: Edit a form
description: You can edit a record in the form view. You can also insert a record, apply a template, and cancel changes to the record.Insert provides a method for creating multiple similar items, such as email notifications, users, groups, or business rules.Your organization may use templates to help with frequently requested tasks. A template contains prepopulated fields that default when the template is selected.Cancel changes to a form by navigating away from the form without saving.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Forms in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Edit a form

You can edit a record in the form view. You can also insert a record, apply a template, and cancel changes to the record.

## Before you begin

Role required: none

## Procedure

1.  Navigate to the form.

    If another user is looking at the same record, you see their avatar with a green dot in the form header. If more than one user is viewing the record, the avatar is a number, and you can point your cursor to it to see the names.

2.  Enter appropriate data.

    Depending on system setup, the data entered in a form can affect other options on the form or change its appearance. For example, if you select a status of **Closed** for an incident, a required **Close Notes** field may appear. Administrators can create custom form effects in various ways, including UI policies and client scripts.

3.  Save the record using one of these methods:

    -   Click **Submit** or **Update** to save changes and return to the previously viewed page.
    -   Right-click the form header and select **Save** to save changes without leaving form view.
    On Core UI forms, fields update dynamically and display a field update icon ![Field update icon](../image/FieldUpdateIconU16.png) to indicate changes made by other users. You can point to the field update icon to see which user made the update. This dynamic indication helps to prevent users from accidentally overwriting each other's work.

    **Note:** If you entered a different value from the value saved by the other user, the system does not update the field automatically. Change your value manually to match value entered by the other user. Otherwise, you overwrite the change when you save the record.


**Parent Topic:**[Forms in the classic environment](../concept/c_UsingForms.md)

## Insert a record

Insert provides a method for creating multiple similar items, such as email notifications, users, groups, or business rules.

### Before you begin

Role required: none

### About this task

Administrators can enable the **Insert** function for task records. For more information, see [Allow insert options on task records](https://www.servicenow.com/docs/access?context=advanced-form-administration&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

### Procedure

1.  Open a similar item.

2.  Edit the item and give it a new **Name**.

3.  Right-click the form header and select one of the following options.

<table id="choicetable_sdh_h2c_br"><tbody><tr><td id="d130067e223">

**Insert**

</td><td>

Saves the item as a new record and returns to the previously viewed page.

</td></tr><tr><td id="d130067e232">

**Insert and Stay**

</td><td>

Saves and views the new record.

</td></tr></tbody>
</table>    ![Insert options](../image/InsertMenuItem.png)


## Apply a template in a form

Your organization may use templates to help with frequently requested tasks. A template contains prepopulated fields that default when the template is selected.

### Before you begin

Role required: none

### Procedure

1.  Navigate to the form.

2.  Do the appropriate action for your version of the UI.

    1.  Click the more options icon \(![More options icon](../image/IconUI16MoreOptions.png)\) in the form header.

    2.  Select **Toggle Template Bar**.

3.  Select the template to apply.

    If there is a conflict between the selected template and the form, a conflict message appears with a link to view the details of the conflict. For example, if a field that does not appear on the form is populated in the template, the conflict message details identify the missing field and the value is not set. If you have a conflict message, review the details and notify your administrator if necessary.

    Specific fields are populated with values from the template.

4.  Complete the form.

    You can change any value that was populated from the template.

5.  Click **Submit** to create the record.


## Cancel changes to a form

Cancel changes to a form by navigating away from the form without saving.

### Before you begin

Role required: none

### Procedure

1.  Navigate away from the form view without saving the record.

2.  If a message appears, click **Leave this Page** to confirm cancellation.

    **Note:** Administrators can disable the confirmation message by setting the **glide.ui.dirty\_form\_support** property to false.


