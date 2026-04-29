---
title: Configure a text command
description: Configure a text command that can be applied by a keyboard shortcut for emails, journal input fields, and HTML fields.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Forms, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure a text command

Configure a text command that can be applied by a keyboard shortcut for emails, journal input fields, and HTML fields.

## Before you begin

Role required: form\_admin, admin

## Procedure

1.  Navigate to `sys_ui_text_command.list`.

    The entire list of UI text commands in the UI Text Command \[sys\_ui\_text\_command\] table opens.

2.  Select **New**.

    A new UI Text Command record opens.

3.  Complete the following fields:

    -   **Name**

        Enter a name for the keyboard shortcut.

    -   **Command Name**

        Enter the key that will apply the command.

        For example, if r is the Command Name, you will need to enter `/r` to apply the keyboard shortcut.

    -   **Description**

        Enter a description of the keyboard shortcut.

    -   **Table**

        Select which table the keyboard shortcut will apply to.

    -   **Applies To**

        Select where the keyboard shortcut will apply from the following options:

        -   **Field Type**

            Apply the keyboard shortcut to either the journal input or HTML field type.

        -   **Email**

            Apply the keyboard shortcut directly to the email composer.

    -   **Field Type**

        Select which field type the keyboard shortcut will apply from the following options:

        -   **Journal Input**

            Apply the keyboard shortcut to journal input fields.

        -   **HTML**

            Apply the keyboard shortcut to HTML fields.

    -   **Action**

        Select an action from the following options:

        -   **Insert Content**

            Add onto existing content.

        -   **Replace Content**

            Replace existing content.

        -   **Custom Event**

            Create a custom event using an action payload.

    -   **Action Script**

        Enter JavaScript code that determines the keyboard shortcut's action.

4.  Select **Submit**.


## Result

The specified keyboard shortcut applies the configured text command.

