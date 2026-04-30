---
title: Configure action items and action steps in offline mode
description: Configure action items to execute actions like create, edit and delete records while in offline mode. For an action item to perform multiple processes you must define separate action steps.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Offline mode, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure action items and action steps in offline mode

Configure action items to execute actions like create, edit and delete records while in offline mode. For an action item to perform multiple processes you must define separate action steps.

## Before you begin

Role required: admin

## About this task

For an action item to work in offline mode you need to define the action item type to be multi-step and at least one action step to have a offline mode option.

## Procedure

1.  Navigate to **All** and in the filter enter `sys_sg_write_back_action_item.list`.

2.  Either select an existing action item or select **New** to create a new action item.

3.  In the **Type** field select **MultiStep**.

4.  Complete the rest of the form as required.

5.  Select **Submit**.

6.  Navigate to **All** and in the filter enter `sys_sg_write_back_action_step.list`.

7.  Either select an existing action step or select **New** to create a new action step.

8.  In the **Writeback Action Item** field, select the action item you created in the earlier steps.

9.  In the **Applicable for** field, select either **Offline** or **Both**.

10. In the **Type** field, select either **New**, **Update** or **Delete**.

11. Complete the rest of the form as required.

12. Select **Submit**.


**Parent Topic:**[Offline mode](../concept/mobile-offline-mode.md)

