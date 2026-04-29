---
title: Set up a form header in CSM Configurable Workspace
description: You can create a form header for use in CSM Configurable Workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Set up a form header in CSM Configurable Workspace

You can create a form header for use in CSM Configurable Workspace.

## Before you begin

Role required: workspace\_admin, ui\_builder\_admin, admin

## About this task

After creating a form header, you must link it to a form header configuration if you want it to appear in CSM Configurable Workspace.

**Note:** You can also use form headers from CSM Agent Workspace in CSM Configurable Workspace if you link the setting to the form header configuration.

One form header configuration **CSM/FSM Configurable Workspace Header Config**, is included with CSM Configurable Workspace. You can use this configuration out of the box without completing any additional configuration steps.

## Procedure

1.  Create a form header.

    1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Configuration Settings** &gt; **UX Form Header**.

    2.  Select **New** on the Form Headers list.

    3.  Fill in the fields on the Form Header form.

<table id="table_lhn_gyx_s3b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Table that is associated with this form header. Whenever an agent selects a record from this table, this form header appears.

</td></tr><tr><td>

Primary field

</td><td>

Field that appears on the top of the form header and acts like the title of the record. Normally, the field is unique and descriptive, such as **short\_description**. This field helps the agent understand what the record is about.

</td></tr><tr><td>

Subheading

</td><td>

Value displayed on the form header that is dependent on the Table selection.

</td></tr><tr><td>

Header Image

</td><td>

Image to display on the workspace form header from an image field. Header images give context to records. They can be set to show agent avatars, differentiate between domains, etc.**Note:** Header images are can only be selected from user image files.

</td></tr><tr><td>

Hide Tags

</td><td>

Toggle to hide tags.

</td></tr><tr><td>

Ignore Highlight

</td><td>

Toggle to turn off \(selected\) highlighting in the form header for fields configured to be highlighted.

</td></tr><tr><td>

Application

</td><td>

Scope of this setting's applicability. Global means that all workspaces can use this setting.

</td></tr><tr><td>

Workspace

</td><td>

Workspace that is associated with this form header.

</td></tr></tbody>
</table>    4.  Select **Submit**.

2.  Add the form header to the form header configuration.

    1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Configuration Settings** &gt; **UX Header Configurations**.

    2.  Select the header configuration.

    3.  In the Workspace Form Headers related list, select **Edit**.

        **Note:** You may need to configure the form to display the related list.

    4.  Move the desired form header from the left column to the right column to add it to the header configuration.

    5.  Select **Save**.


**Related topics**  


[Configure a form header for a workspace](https://www.servicenow.com/docs/access?context=config-ws-form-header&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)

