---
title: Create a list or related list action button
description: Create a list or related list action and add the button to a workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/create-a-new-list-or-related-list-action.html
release: zurich
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create action buttons, Declarative actions, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Create a list or related list action button

Create a list or related list action and add the button to a workspace.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Declarative Actions** &gt; **Create new action**.

2.  Select **List** or **Related List**.

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
    -   **Icon**

        The icon for the action.

        **Note:** Select **ai-sparkle-fill** to add the ServiceNow Otto icon. For hover animation, select the Animate icon check box.

    -   **Button type**

        The color variant of the action button.

        **Note:** **AI Primary**, **AI Secondary**, and **AI Tertiary** are AI gradient variants that visually indicate when users are interacting with AI-powered experiences.

    -   **Record Selection Required**

        When selected, the action requires one or more records to be selected.

    -   **Application**

        The scope that the action exists within.

    -   **Table**

        Table for the action button to appear on.

    -   **View**

        UI view for the action button to appear on.

    -   **Experience Restricted**

        When selected, the action is limited to an experience instead of being available across all experiences.

    -   **Active**

        When selected, the action is active.

    -   **Order**

        Order in which the action appears relative to other actions.

    -   **Group By**

        When selected, the action appears under a selected group.

    -   **Group**

        The group that the action appears under. Applicable when the Group By check box is selected.

    -   **Tooltip**

        Tooltip text that appears for the action.

    -   **Description**

        Description of the action for internal reference.

4.  Select **Submit**.


## Result

The list or related list action button appears within the workspace you specified.

## What to do next

Configure a button to apply an action in the following ways:

-   **Trigger a UI interaction from a declarative action**

    Trigger a UI interaction from a declarative action to extend a page without taking ownership.

-   **[Configure dynamic conditions for a list action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/disable-list-actions-based-on-dynamic-conditions.md)**

    Configure a list or related list action to perform an action only when it satisfies dynamic conditions.


