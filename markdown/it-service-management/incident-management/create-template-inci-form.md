---
title: Create a template from the incident form
description: Create a template that defines default values for the Incident form so that users don't have to enter the same values each time they create an incident.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/create-template-inci-form.html
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Managing incidents, Incident Management, IT Service Management]
---

# Create a template from the incident form

Create a template that defines default values for the Incident form so that users don't have to enter the same values each time they create an incident.

## Before you begin

Role required: itil, sn\_incident\_write, or admin

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Create**.

2.  Select the More options icon \[Omitted image "more-options.png"\] Alt text: and then select **Toggle Template Bar** to see the template bar.

    \[Omitted image "toggle-template-bar.png"\] Alt text: More options menu showing the Toggle Template Bar option

3.  On the template bar, select the Create New Template icon \[Omitted image "add\_icon.png"\] Alt text:.

    \[Omitted image "create-template-inci-form.png"\] Alt text: Template bar showing the Create New Template icon

4.  On the form, fill in the fields.

<table id="table_j3z_w3k_wmb"><thead><tr><th>

Field

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

Application scope of the template. The scope defines whether the template is available for all applications or for scoped applications.

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

Option for allowing any user with the itil, sn\_incident\_write, or admin role to view and apply this template. When you clear this option, only users or groups specified in the **User** and **Groups** fields can access the template.

</td></tr><tr><td>

Short description

</td><td>

Description of the template.**Note:** Adding content to this field doesn't add that content to the **Short description** field of the forms that use this template.

</td></tr><tr><td>

Template

</td><td>

Content that automatically populates records that are based on this template. Select a field from the specified table in the left column and then enter the data to automatically populate in the right column.**Note:** Even though you can select dot-walked fields in the template, they don't apply to fields that are on the form.

</td></tr></tbody>
</table>5.  Select **Submit**.

    The template is created and you can find it on the template bar.


