---
title: Configure the HTML editor toolbar for journal fields
description: Configure toolbar options for the HTML editor within journal input fields.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Forms, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure the HTML editor toolbar for journal fields

Configure toolbar options for the HTML editor within journal input fields.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table opens.

2.  Configure HTML plugins for journal input fields.

    1.  Add a system property named **glide.ui.journal.html.plugins**.

        For more information on adding system property, see Add a system property.

    2.  Select **Submit**.

3.  Configure the HTML editor toolbar for journal input fields.

    1.  Add a system property named **glide.ui.journal.html.toolbar**.

        For more information on adding system property, see Add a system property.

    2.  Select **Submit**.

4.  Configure what happens when you press Enter \(Windows\) or Return \(Mac\) within journal fields.

    1.  From the System Properties list, select the **glide.ui.journal.newline\_behavior** system property.

        A System Property record opens.

    2.  In the Value field, enter one of the following options:

        -   **`default`**

            When you press Enter \(Windows\) or Return \(Mac\), the HTML editor inserts a block.

            When you press Shift+Enter \(Windows\) and Shift+Return \(Mac\), the HTML editor inserts a br tag.

        -   **`block`**

            The HTML editor inserts a block in all cases.

        -   **`linebreak`**

            The HTML editor inserts a br tag in all cases.

        -   **`invert`**

            When you press Enter \(Windows\) or Return \(Mac\), the HTML editor inserts a br tag.

            When you press Shift+Enter \(Windows\) and Shift+Return \(Mac\), the HTML editor inserts a block.

    3.  Select **Update**.


