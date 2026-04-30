---
title: Set up a form header in CSM Configurable Workspace
description: You can create a form header for use in CSM Configurable Workspace.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Set up a form header in CSM Configurable Workspace

You can create a form header for use in CSM Configurable Workspace.

## Before you begin

Role required: workspace\_admin, ui\_builder\_admin, admin

## About this task

After creating a form header, you must link it to a form header configuration if you want it to appear in CSM Configurable Workspace.

**Note:** You can also use form headers from CSM Agent Workspace in CSM Configurable Workspace if you link the setting to the form header configuration.

One form header configuration **CSM/FSM Configurable Workspace Header Config**, is included with CSM Configurable Workspace. You can use this configuration out of the box without completing any additional configuration steps.

## Procedure

1.  Create a form header.

    1.  Navigate to **Now Experience Framework** &gt; **Configuration Settings** &gt; **UX Form Header**.

    2.  Select **New** on the Form Headers list.

    3.  Fill in the fields on the form header form.

        For field descriptions, see Set up form headers in workspace.

    4.  Select **Submit**.

2.  Add the form header to the form header configuration.

    1.  Navigate to **Now Experience Framework** &gt; **Configuration Settings** &gt; **UX Header Configurations**.

    2.  Select the header configuration.

    3.  In the Workspace Form Headers related list, select **Edit**.

        **Note:** You might have to configure the form to display the related list.

    4.  Move the desired form header from the left column to the right column to add it to the header configuration.

    5.  Select **Save**.


