---
title: Create an attachment action button
description: Create an attachment action and add the button to a workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/create-a-new-attachment-action.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create action buttons, Declarative actions, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Create an attachment action button

Create an attachment action and add the button to a workspace.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Declarative Actions** &gt; **Create new action**.

2.  Select **Attachment**.

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
    -   **Animate icon**

        When selected, the icon is animated.

    -   **Application**

        The scope that the action exists within.

    -   **Workspace**

        The workspace for the action button to appear on.

    -   **Table**

        Table for the action button to appear on.

    -   **View**

        UI view for the action button to appear on.

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

The attachment action button appears within the workspace you specified.

