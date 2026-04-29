---
title: Create a form action button
description: Create a form action and add the button to a workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create action buttons, Declarative actions, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Create a form action button

Create a form action and add the button to a workspace.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Declarative Actions** &gt; **Create new action**.

2.  Select **Form**.

    A new Action Assignment record opens.

3.  Complete the following fields:

    -   **Action label**

        Enter a label for the action.

    -   **Action name**

        This field will populate automatically with the action label in all lowercase and with spaces replaced with underscores.

    -   **Implemented as**
        -   Select **Server Script** to apply the action to the server or database as JavaScript.
        -   Select **UXF Client Action** to apply the action as a UI Builder page event.
        -   Select **Client Script** to apply the action to the web browser as JavaScript.
        -   Select **UI interaction** to apply the action as reusable logic and UI elements. For configuration instructions, see [Trigger a UI interaction from a declarative action](../task/configure-da-ui-interactions.md).
    -   **Table**

        Select a table for the action button to appear on.

    -   **View**

        Select a UI view for the action button to appear on.

4.  Select the Additional actions icon \(![menu icon](../../workspace/image/menu-icon-save.png)\) and **Save**.

5.  From the Layout Items related list, select your action.

    You can also select the **UX Form Layout Item** link in the form message.

    A UX Form Actions Layout Item record opens.

6.  Complete the following fields to update the look and feel of the button:

    -   **Icon**

        Select an icon for the action.

    -   **Color**

        Select a color for the action. You have access to choose any color the button component supports.

7.  Select **Update**.


## Result

The form action button appears within the workspace you specified.

## What to do next

Configure a button to apply an action in the following ways:

-   **[Trigger a UI interaction from a declarative action](../task/configure-da-ui-interactions.md)**

    Trigger a UI interaction from a declarative action to extend a page without taking ownership.

-   **[Configure a form action to open a custom modal](configuring-an-action-button-to-open-a-custom-modal.md)**

    Configure a declarative action to open a custom modal that provides information or interactive elements without navigating away from the current page.


