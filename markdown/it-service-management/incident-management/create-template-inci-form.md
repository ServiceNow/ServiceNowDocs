---
title: Create a template from the incident form
description: Create a template that define default values for forms so that users can easily create incident. You need to have appropriate permissions before creating templates.
locale: en-US
release: yokohama
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage, Incident Management, IT Service Management]
---

# Create a template from the incident form

Create a template that define default values for forms so that users can easily create incident. You need to have appropriate permissions before creating templates.

## Before you begin

Role required: itil, sn\_incident\_write, or admin

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Create**.

2.  Click the more options icon ![More options icon](../../change-management/image/more-options.png) and then click **Toggle Template Bar** to see the template bar.

    ![Toggle template bar](../image/toggle-template-bar.png)

3.  On the template bar, click the add icon \(![Add icon](../image/add_icon.png)\).

    ![Click add to create template.](../image/create-template-inci-form.png)

4.  On the form, fill in the fields.

<table id="table_j3z_w3k_wmb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the template.

</td></tr><tr><td>

Table

</td><td>

Table that this template applies to. Select **Global** to make the template available for use with all tables.**Note:** The table list shows only the tables and database views that are in the same scope as the template.

</td></tr><tr><td>

Active

</td><td>

Option for making the template available for use. A template must be active to be used.

</td></tr><tr><td>

Application

</td><td>

Application scope of the rules. The scope defines whether the rules are available for all applications or for scoped applications.

</td></tr><tr><td>

User

</td><td>

User who can configure and apply the template. If you define a user, no other users can see the template unless you select the **Global** option.

</td></tr><tr><td>

Groups

</td><td>

Group whose members can configure and apply the template. If you define a group, no other groups can see the template unless you select the **Global** option.

</td></tr><tr><td>

Global

</td><td>

Option for allowing any user who can access the templates to view and apply this template.

</td></tr><tr><td>

Short description

</td><td>

Description of the template.**Note:** Adding content to this field does not add that content to the **Short description** field of the forms that use this template.

</td></tr><tr><td>

Template

</td><td>

Content that automatically populates records that are based on this template. Select a field from the specified table in the left column and then enter the data to automatically populate in the right column.**Note:** Even though you can select dot-walked fields in the template, they do not apply to fields that are on the form.

</td></tr></tbody>
</table>5.  Click **Submit**.

    The template is created and you can find it on the template bar.


