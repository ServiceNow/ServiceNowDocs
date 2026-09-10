---
title: Configure a form action layout item
description: Customize the appearance of a form action and control how it appears relative to other actions in a table layout.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/configure-form-action-layout-item.html
release: zurich
topic_type: task
last_updated: "2026-09-03"
reading_time_minutes: 1
breadcrumb: [Create action buttons, Declarative actions, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure a form action layout item

Customize the appearance of a form action and control how it appears relative to other actions in a table layout.

## Before you begin

Create a declarative action and add the button to a workspace. For instructions, see [Creating declarative action buttons](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/creating-declarative-actions.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Declarative Actions** &gt; **Form Actions**.

2.  Select a form action.

    An Action Assignment record opens.

3.  From the Layout Items related list, select a layout item.

    A UX Form Actions Layout Item record opens.

4.  Complete the following fields:

    -   **Name**

        The name of the layout item.

    -   **Label**

        The label for the layout item.

    -   **Item Type**

        The type of layout item.

    -   **Action**

        The form action that the layout item represents. Applicable when the Item Type field is set to **Action**.

    -   **Group**

        The form action layout group that the layout item represents. Applicable when the Item Type field is set to **Group**.

    -   **Overflow**

        When selected, the action appears in the overflow menu.

    -   **Icon**

        The icon for the layout item.

        **Note:** Select **ai-sparkle-fill** to add the ServiceNow Otto icon. For hover animation, select the Animate icon check box.

    -   **Color**

        The color variant of the layout item.

        **Note:** **AI Primary**, **AI Secondary**, and **AI Tertiary** are AI gradient variants that visually indicate when users are interacting with AI-powered experiences.

    -   **Application**

        The scope that the action exists within.

    -   **Table**

        Table for the layout item to appear on.

    -   **Order**

        Order in which the action appears relative to other actions.

    -   **Active**

        When selected, the layout item is active.

    -   **Description**

        Description of the layout item for internal reference.

5.  Select **Update**.


