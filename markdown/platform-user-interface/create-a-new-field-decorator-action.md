---
title: Create a field decorator action button
description: Create a field decorator action and add the button to a workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create action buttons, Declarative actions, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Create a field decorator action button

Create a field decorator action and add the button to a workspace.

## Before you begin

Role required: admin

**Note:** Field decorators can only be configured for single-line string fields. Multi-line fields do not support field decorators.

## Procedure

1.  Navigate to **All** &gt; **Declarative Actions** &gt; **Create new action**.

2.  Select **Field decorator**.

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
    -   **Table**

        Select a table for the action button to appear on.

    -   **View**

        Select a UI view for the action button to appear on.

4.  Select **Submit**.


## Result

The field decorator action button appears within the workspace you specified.

