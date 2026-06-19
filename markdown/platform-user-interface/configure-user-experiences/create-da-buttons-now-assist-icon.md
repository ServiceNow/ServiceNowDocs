---
title: Configure a declarative action with the Now Assist icon
description: Configure a declarative action button with the Now Assist icon \(\) and hover animation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/configure-user-experiences/create-da-buttons-now-assist-icon.html
release: zurich
product: Configure User Experiences
classification: configure-user-experiences
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [declarative actions]
breadcrumb: [Configure action buttons, Declarative actions, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure a declarative action with the Now Assist icon

Configure a declarative action button with the Now Assist icon \(\[Omitted image "icon-ai-sparkle.png"\]\) and hover animation.

## Before you begin

Create a declarative action and add the button to a workspace. For instructions, see [Creating declarative action buttons](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/creating-declarative-actions.md).

Role required: admin

## About this task

The Now Assist icon \(\[Omitted image "icon-ai-sparkle.png"\]\) with hover animation is supported for buttons and split buttons. If the action falls into the overflow or acts as a subitem in a split button, the hover animation doesn't work.

## Procedure

1.  Navigate to **All** &gt; **Declarative Actions** and select the action type that matches your action.

2.  From the Action Assignment list, select an action.

3.  In the Icon field, selecting **ai-sparkle-fill** to add the Now Assist icon \(\[Omitted image "icon-ai-sparkle.png"\]\).

    **Important:** For adding the Now Assist icon \(\[Omitted image "icon-ai-sparkle.png"\]\) to a form action, find the Icon field by first selecting a layout item from the Layout Items related list.

    Layout items control how declarative actions appear relative to other actions in a table layout. If your action is associated with multiple layouts, you might see multiple entries.

4.  Add hover animation to the icon by selecting **Animate icon**.

5.  Select **Update**.


