---
title: Set up a form header in CRM Workspace
description: You can create a form header for use in CRM Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/config-csm-config-ws-form-header.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Set up CRM Workspace, CRM Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Set up a form header in CRM Workspace

You can create a form header for use in CRM Workspace.

## Before you begin

Role required: workspace\_admin, ui\_builder\_admin, admin

## About this task

Form headers in CRM Workspace provide a quick glance of case, account, or contact information. They include a primary value and several secondary values. You can configure the information that appears in the form header for the Case, Account, and Contact forms. You can also configure the placement of the secondary values.

After creating a form header, you must link it to a form header configuration if you want it to appear in CRM Workspace.

One form header configuration, CRM Workspace Header Config, is included with CRM Workspace. You can use this configuration without completing any additional configuration steps.

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

3.  Configure the placement of the secondary values in the form header.

    1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Experiences** &gt; **CRM Workspace.**.

    2.  In the UX Page Properties list, select the form header property.

        For example, select **configHeaderId** to display the page property form. The **Value** field determines the placement of the secondary values.

    3.  Enter the location of the secondary values in the **Values** field.

        -   **sidebar**: The secondary values appear in the contextual side panel.
        -   **header**: The secondary values appear in the header along with the primary value.
    4.  Select **Save**.


**Related topics**  


[Configure a form header for a workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/config-ws-form-header.md)

