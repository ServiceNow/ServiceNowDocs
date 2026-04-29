---
title: Configure dynamic conditions for a list action
description: Configure a list or related list action to perform an action only when it satisfies dynamic conditions.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure action buttons, Declarative actions, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure dynamic conditions for a list action

Configure a list or related list action to perform an action only when it satisfies dynamic conditions.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Declarative Actions** and select either **List Actions** or **Related List Actions**.

2.  From the Action Assignment list, select an action.

    An Action Assignment record opens.

3.  Select the **Record Selection Required** checkbox.

4.  Select the **Experience Restricted** checkbox.

5.  From the Conditions section, complete the following fields:

    -   **Enable Dynamic Evaluation**

        Select the checkbox.

    -   **Dynamic Script Condition**

        Write a scripted condition for dynamic evaluation.

    -   **Dynamic Record Conditions**

        Add conditions for dynamic evaluation if you don't want to write a scripted condition.

6.  Select **Update**.


## Result

The action will only be available when selected list items satisfy the dynamic conditions.

**Note:** You may experience slowness and unresponsiveness if this feature is used in combination with **Select All**, which selects all records in a list, as conditions must be evaluated for all of the selected records.

