---
title: Display and hide buttons in offline mode
description: Define whether to show or hide buttons while users are in offline mode on their Mobile Agent app.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure properties/action functions, Offline mode, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Display and hide buttons in offline mode

Define whether to show or hide buttons while users are in offline mode on their Mobile Agent app.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** and in the filter enter `sys_sg_button.list`.

2.  Select an existing action function or select **New**.

    The Function screen displays. For more information on how to configure an action function, see [Action functions](../concept/mobile-actions.md).

3.  Select the **Offline Properties** tab.

4.  Select the **Offline** check box to display all the fields relevant for an offline function configuration.

5.  Complete the action function offline mode property fields as required, see [Configure offline mode properties for action functions](config-offline-properties-action-funct.md).

6.  From the **Offline Condition Type** field, select whether the condition style is **Declarative** or **Script**.

7.  From the **Table** field, select a table that is the source of the fields used in the **Offline Condition** field, and from where the conditions are evaluated.

8.  Depending on the selection made from the **Offline Condition Type** field, either do one of the following in the **Offline Condition** field:

    -   For **Declarative**, create declarative conditions to be performed in offline mode.
    -   For **Script**, enter a script in the text window that contains query conditions that are evaluated in offline mode.
9.  Select **Submit** to save your display and hide button configurations.


**Parent Topic:**[Configure offline mode properties for action functions](config-offline-properties-action-funct.md)

