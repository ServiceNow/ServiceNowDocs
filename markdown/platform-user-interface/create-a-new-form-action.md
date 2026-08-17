---
title: Create a form action button
description: Create a form action button for a Configurable Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/create-a-new-form-action.html
release: australia
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [Create action buttons, Declarative actions, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Create a form action button

Create a form action button for a Configurable Workspace.

## Before you begin

Role required: admin

## About this task

\[Omitted video\] Description: Procedural video for creating a form action button

## Procedure

1.  Navigate to **All** &gt; **Declarative Actions** &gt; **Create New Action**.

2.  Select **Form** from the list of action types.

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
    -   **Application**

        The scope that the action exists within.

    -   **Table**

        Table for the action button to appear on.

    -   **View**

        UI view for the action button to appear on.

    -   **Enable for all Configurable Experiences**

        When selected, the action is visible in all Configurable Experiences.

    -   **Active**

        When selected, the action is active.

    -   **Order**

        Order in which the action appears relative to other actions.

    -   **Tooltip**

        Tooltip text that appears for the action.

    -   **Description**

        Description of the action for internal reference.

4.  Select **Submit**.


## Result

The form action button is created and scoped to the table and view you specified.

## What to do next

Configure a button to apply an action in the following ways:

-   **[Trigger a UI interaction from a declarative action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-da-ui-interactions.md)**

    Trigger a UI interaction from a declarative action to extend a page without taking ownership.

-   **[Configure a form action to open a custom modal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configuring-an-action-button-to-open-a-custom-modal.md)**

    Configure a declarative action to open a custom modal that provides information or interactive elements without navigating away from the current page.


