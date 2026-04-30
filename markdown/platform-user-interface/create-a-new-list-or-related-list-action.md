---
title: Create a list or related list action button
description: Create a list or related list action and add the button to a workspace.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
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

        Enter a label for the action.

    -   **Action name**

        This field will populate automatically with the action label in all lowercase and with spaces replaced with underscores.

    -   **Implemented as**

        Select **Server Script** to apply the action to the server or database as JavaScript.

        Select **UXF Client Action** to apply the action as a UI Builder page event.

        Select **Client Script** to apply the action to the web browser as JavaScript.

    -   **Table**

        Select a table for the action button to appear on.

    -   **View**

        Select a UI view for the action button to appear on.

4.  Select **Submit**.


## Result

The list or related list action button appears within the workspace you specified.

## What to do next

Configure a button to apply an action in the following ways:

-   **[Configure dynamic conditions for a list action](../../workspace/task/disable-list-actions-based-on-dynamic-conditions.md)**

    Configure a list or related list action to perform an action only when it satisfies dynamic conditions.


