---
title: Create a field decorator action button
description: Create a field decorator action and add the button to a workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/create-a-new-field-decorator-action.html
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

        The label for the action.

    -   **Action name**

        Action label populates automatically in all lowercase and with spaces replaced with underscores.

    -   **Implemented as**
        -   **Server Script** applies the action to the server or database as JavaScript.
        -   **UXF Client Action** applies the action as a UI Builder page event.
        -   **Client Script** applies the action to the web browser as JavaScript.
    -   **Decorator applies to**

        Where the decorator should appear. Only three decorators may appear on a single field at one time.

    -   **Field type**

        The field type that displays the decorator. Applicable when the Decorator applies to field is set to **Field type**.

    -   **Icon**

        The icon for the action.

        **Note:** Select **ai-sparkle-fill** to add the ServiceNow Otto icon.

    -   **Application**

        The scope that the action exists within.

    -   **Workspace**

        The workspace for the action button to appear on.

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

    -   **Tooltip**

        Tooltip text that appears for the action.

    -   **Description**

        Description of the action for internal reference.

4.  Select **Submit**.


## Result

The field decorator action button appears within the workspace you specified.

