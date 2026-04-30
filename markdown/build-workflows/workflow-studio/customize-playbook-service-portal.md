---
title: Customize the playbook in Service Portal
description: Use the Service Portal Designer to customize the playbook runtime experience for Service Portal users.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Playbooks in Service Portal, Designing playbooks, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Customize the playbook in Service Portal

Use the Service Portal Designer to customize the playbook runtime experience for Service Portal users.

## Before you begin

-   Role required: admin, or portal admin with either snc\_internal or snc\_external
-   Create a record generator if you don't want to use the default record generator or any of the other existing record generators.

    **Note:** A key difference in Service Portal is that the playbook record generator is used instead of the record producer. The Service Portal requester enters the information for the record generator and uses the Next or Continue declarative action to move to the next activity​.

    To learn more about playbook record generators, see .


## Procedure

1.  To edit your playbook widget in the Service Portal Designer, navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration**.

2.  Select **Page Editor**.

3.  Search for and select your playbook.

4.  Select **Edit \[Playbook\] \(playbook\) page in Designer**.

5.  Select the widget, and select the edit icon.

    |Field|Description|
    |-----|-----------|
    |Playbook UIB Page URL|Enter a URL for the UI Builder page. If not specified, this points to the default **Playbook Experience Portal** page.|
    |Open Record Widget|The Sys ID for the widget to use when a user opens a record. If not specified, the form widget is used.|
    |Open Record is Pop Up|If enabled, shows the reference picker inside the form.|
    |Open List Widget|The Sys ID for the widget to use when a user opens a list. If not specified, the Data Table from the Instance Definition is used.|
    |Extra Params|Pass arbitrary data from the widget to its UI Builder page.|

<table id="table_lbs_h1h_sbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Height

</td><td>

Enter the height of the playbook. If not specified, height is set to 850px.

</td></tr><tr><td>

Open Record Modal Title

</td><td>

Add a title to the modal that a user sees whenever they open a record. If not specified, there is no title.

</td></tr><tr><td>

Open Record Modal Message

</td><td>

Add a message to the modal that a user sees whenever they open a record. If not specified, there is no message.

</td></tr><tr><td>

Open Record Modal Buttons

</td><td>

Add the buttons to the modal that a user sees whenever they open a record. If not specified, there are no buttons. Enter in JSON format.

</td></tr><tr><td>

Open Record Modal View

</td><td>

The form view that you want to show for the open record.

</td></tr><tr><td>

Open Record Modal Size

</td><td>

Choose the size of the modal that a user sees whenever they open a record. Choice are:-   sm - small
-   md - medium
-   lg - large
If not specified, defaults to large.

</td></tr><tr><td>

Open List Modal Title

</td><td>

Add a title to the modal that a user sees whenever they open a list. If not specified, there is no title.

</td></tr><tr><td>

Open List Modal Message

</td><td>

Add a message to the modal that a user sees whenever they open a list. If not specified, there is no message.

</td></tr><tr><td>

Open List Modal Buttons

</td><td>

Add the buttons to the modal that a user sees whenever they open a list. If not specified, there are no buttons. Enter in JSON format.

</td></tr><tr><td>

Open List Modal View

</td><td>

The form view that you want to show for the open list.

</td></tr><tr><td>

Open List Modal Size

</td><td>

Choose the size of the modal that a user sees whenever they open a list. Choice are:-   sm - small
-   md - medium
-   lg - large
If not specified, defaults to large.

</td></tr><tr><td>

Activity View

</td><td>

Change the activity view between stacked or focused.

</td></tr><tr><td>

Playbook Experience ID

</td><td>

Enter the playbook experience record ID with the playbook configurations that you want for your Service Portal users. When nothing is set in the URL during the playbook run, this is the default playbook experience. If nothing is specified here, defaults to the Global Playbook Experience.

</td></tr><tr><td>

Open Record Modal Prevent URL Update on Submit

</td><td>

Prevents the URL of a running playbook in Service Portal from updating whenever a new record is submitted from a form in a record modal.

</td></tr></tbody>
</table>
Verify that you are using the official Playbook Widget for the Portal Page.

**Parent Topic:**[Playbooks in Service Portal](../concept/playbooks-service-portal.md)

