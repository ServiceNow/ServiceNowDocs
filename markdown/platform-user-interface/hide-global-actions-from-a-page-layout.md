---
title: Hide global form actions from a page layout
description: Exclude global form actions from a page or experience by using action layouts.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Customizing Configurable Workspace with declarative actions, Administering Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Hide global form actions from a page layout

Exclude global form actions from a page or experience by using action layouts.

## Before you begin

Role required: admin

## Procedure

1.  In the navigation filter, navigate to **All** &gt; **Declarative Actions** &gt; **Form Action Layouts**.

2.  Open an existing layout.

    Your scope must match the application of the record.

    **Important:** Any form action layouts created in Washington DC or later are unified automatically. You will need to associate any new form actions including global form actions manually.

3.  Use the related list to control the display of the actions in this layout.

4.  Open your record page in UI Builder.

5.  Open the data module.

6.  Select the record controller or data broker.

7.  Select the existing layout from the Action layout property list and select **Save**.

8.  View the page at runtime.


## Result

The actions match the layout specified. Not all of the actions might be visible in the layout. Only actions that meet the requirements appear.

