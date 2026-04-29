---
title: Set up a form action in CSM Configurable Workspace
description: Create a form action that links to a UI action so that you can use the UI action in CSM Configurable Workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-18"
reading_time_minutes: 1
breadcrumb: [Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Set up a form action in CSM Configurable Workspace

Create a form action that links to a UI action so that you can use the UI action in CSM Configurable Workspace.

## Before you begin

Role required: workspace\_admin, ui\_builder\_admin, admin

## About this task

In order to use UI actions in CSM Configurable Workspace, each UI action must have a corresponding form action.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Declarative Actions** &gt; **Create New Action**.

2.  Select **Form** from the list of available actions.

3.  Fill in the following fields on the Action Assignment form.

<table id="choicetable_zhx_pfj_q3c"><thead><tr><th align="left" id="d178991e101">

Field

</th><th align="left" id="d178991e104">

Description

</th></tr></thead><tbody><tr><td id="d178991e110">

**Action label**

</td><td>

The name of the action. For example, Create or Save.

</td></tr><tr><td id="d178991e119">

**Action name**

</td><td>

This field populates automatically with the action label in all lowercase and with spaces replaced with underscores.

</td></tr><tr><td id="d178991e128">

**Implemented as**

</td><td>

Select one of the following:-   Server Script: Applies the action to the server or database as JavaScript.
-   UXF Client Action: Applies the action as a UI Builder page event.
-   Client Script: Applies the action to the web browser as JavaScript.


</td></tr><tr><td id="d178991e148">

**Table**

</td><td>

Select a table for the action button to appear on.

</td></tr><tr><td id="d178991e158">

**View**

</td><td>

Select a UI view for the action button to appear on.

</td></tr></tbody>
</table>4.  Select the Additional Actions icon and select **Save**.

5.  From the Layout Items related list, select your action to display the UX Form Actions Layout Item record.

6.  Complete the following fields to update the look and feel of the action.

    |Field|Description|
    |-----|-----------|
    |**Icon**|Select an icon for the action.|
    |**Color**|Select a color for the action. You have access to choose any color the button component supports.|

7.  Select **Update**.


