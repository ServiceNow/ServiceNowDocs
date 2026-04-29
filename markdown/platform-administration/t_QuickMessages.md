---
title: Define a quick message
description: Create predefined content to add in the email client so that users can write emails consistently and efficiently.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Composing emails with quick messages, Configure, Email client, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Define a quick message

Create predefined content to add in the email client so that users can write emails consistently and efficiently.

## Before you begin

Role required: email\_client\_quick\_message\_author or admin

## Procedure

1.  Navigate to **Email Client** &gt; **Quick Messages**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_fsj_rkm_qq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Name that appears in the Quick Message selector.

</td></tr><tr><td>

Active

</td><td>

Option for activating the quick message. When selected, the quick message is available for selection in the Quick Message selector.

</td></tr><tr><td>

Application

</td><td>

Type of scoped application.

</td></tr><tr><td>

User

</td><td>

User who has access to this quick message. Selecting a user restricts access to that user only. Leave the field blank to have no user-based restrictions.

</td></tr><tr><td>

Group

</td><td>

Group whose members have access to this quick message. Selecting a group restricts access to members of that group only. Leave the field blank to have no group-based restrictions.

</td></tr><tr><td>

Table

</td><td>

Table to which the quick message applies. To make the quick message available for all tables, leave blank.

</td></tr><tr><td>

Conditions

</td><td>

Target record that must match the conditions before the quick message appears for selection in the email client.

</td></tr><tr><td>

Body

</td><td>

Content to insert in the **Message Text** field in the email client. By default, the field supports HTML format.

 To reference field values, select variables from the variables list or manually type variable references using the syntax `${table_name.variable_name}`. To reference the user who launches the email client, enter the variable `${current_user}`. To reference the title of the user who launches the email client, enter the variable `${current_user.title}`.

 **Note:** To view and select the variables, you must select a Table.

 You can use these values to include a predefined signature in email responses from agents to customers.

 **Note:** Line breaks don't appear for multi-line fields such as $\{description\} and $\{comments\} in the email client template.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Composing emails with quick messages](../concept/quick-message.md)

