---
title: Create a form action button
description: Create a form action button and configure it to appear in a workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/create-a-new-form-action.html
release: australia
topic_type: task
last_updated: "2026-06-25"
reading_time_minutes: 1
breadcrumb: [Create action buttons, Declarative actions, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Create a form action button

Create a form action button and configure it to appear in a workspace.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Declarative Actions** &gt; **Create new action**.

2.  Select **Form**.

    A new Action Assignment record opens.

3.  Complete the following fields:

    -   **Action label**

        The label for the action.

    -   **Action name**

        Action label populates automatically in all lowercase and with spaces replaced with underscores.

    -   **Implemented as**
        -   **Server Script** applies the action to the server or database as JavaScript.
        -   **UXF Client Action** applies the action as a UI Builder page event.
        -   **Client Script** applies the action to the web browser as JavaScript.
        -   **UI interaction** applies the action as reusable logic and UI elements. For configuration instructions, see [Trigger a UI interaction from a declarative action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-da-ui-interactions.md).
    -   **Table**

        Table for the action button to appear on.

    -   **View**

        UI view for the action button to appear on.

4.  Select the Additional actions icon \(\[Omitted image "menu-icon-save.png"\] Alt text:\) and **Save**.

5.  From the Layout Items related list, select your action.

    You can also select the **UX Form Layout Item** link in the form message.

    A UX Form Actions Layout Item record opens.

6.  Complete the following fields to update the look and feel of the button:

    -   **Icon**

        Icon for the action.

    -   **Color**

        Colors supported by the button component.

7.  Select **Update**.


## Result

The form action button appears within the workspace you specified.

## What to do next

Configure a button to apply an action in the following ways:

-   **[Trigger a UI interaction from a declarative action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-da-ui-interactions.md)**

    Trigger a UI interaction from a declarative action to extend a page without taking ownership.

-   **[Configure a form action to open a custom modal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configuring-an-action-button-to-open-a-custom-modal.md)**

    Configure a declarative action to open a custom modal that provides information or interactive elements without navigating away from the current page.


