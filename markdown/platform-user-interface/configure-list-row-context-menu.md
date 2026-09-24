---
title: Configure a row action
description: Create a row action for a Configurable Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/configure-list-row-context-menu.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Create action buttons, Declarative actions, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure a row action

Create a row action for a Configurable Workspace.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Declarative Actions** &gt; **Create New Action**.

2.  Select **Row Actions** from the list of action types.

    A new Action Assignment record opens.

3.  Complete the following fields:

    -   **Action label**

        The label for the action.

    -   **Action name**

        Action label populates automatically in all lowercase and with spaces replaced with underscores.

    -   **UI interaction**

        The implementation that applies the action as reusable logic and UI elements. For configuration instructions, see [Trigger a UI interaction from a declarative action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/configure-da-ui-interactions.md).

    -   **Icon**

        The icon for the action.

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

    -   **Description**

        Description of the action for internal reference.

4.  Select **Submit**.


## Result

The row action button appears within the workspace you specified.

