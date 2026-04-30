---
title: Create a UXF client action for forms
description: Configure a form action as a UXF client action and add the action to an existing layout.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Customizing Configurable Workspace with declarative actions, Administering Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Create a UXF client action for forms

Configure a form action as a UXF client action and add the action to an existing layout.

## Before you begin

Complete the following actions:

-   [Create a form action](create-a-new-form-action.md)
-   Select **UXF Client Action** for the Implemented as field.

**Important:** The steps enable you to add a UXF client action button to your configurable workspace. For instructions on configuring your form action button to open a custom modal, see [Configure action button to open a custom modal](configuring-an-action-button-to-open-a-custom-modal.md).

Role required: admin

This video shows you how to perform the following procedure.Configure a form action as a UXF client action and add the action to an existing layout.

## Procedure

1.  In the navigation filter, navigate to **All** &gt; **Declarative Actions** &gt; **Form actions**.

2.  Open the action assignment for your form action by selecting the action label.

    The **Implemented as** field should be set to **UXF Client Action**.

3.  Select the search icon \(![search icon](../../../use/navigation/image/IconSearch.png)\) in the **Specify client action** field.

4.  Select an existing payload definition.

    For instructions on setting up a new payload definition, see [Configure action button to open a custom modal](configuring-an-action-button-to-open-a-custom-modal.md).

5.  Enter a value in the **Tooltip** field.

6.  Select **Advanced View**.

7.  Navigate to the **Layout Items** tab and select your form action.

8.  In the UX form Actions Layout Item page, select an icon, color for the button, and **Save**.

9.  Select **Edit** in the UXF Client Actions list.

10. Add a table to the action by selecting a table from the Collection lists, adding it into the UX Form Action Layouts list, and selecting **Save**.

11. Return to the action assignment page for the form action.

12. Navigate to the Action Configurations tab and select **Edit**.

13. Add an action configuration by selecting a configuration from the Collections list, adding it to the Action Configurations list, and selecting **Save**.


## Result

Your form action appears in the list of form action layouts. Your form action button appears within your configurable workspace.

