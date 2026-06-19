---
title: Configure action items and action steps in offline mode
description: Configure action items to execute actions like create, edit and delete records while in offline mode. For an action item to perform multiple processes you must define separate action steps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/configure-action-item-offline.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Action items/action steps, Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure action items and action steps in offline mode

Configure action items to execute actions like create, edit and delete records while in offline mode. For an action item to perform multiple processes you must define separate action steps.

## Before you begin

Role required: mobile\_admin, admin

## About this task

For an action item to work in ofﬂine mode, you must deﬁne the action item type to be multi-step and at least one action step to have an ofﬂine mode option and at least one online mode option. Offline steps only affect the local database on the user's device, so any offline step that modifies local data must have a corresponding online step to update the instance database.

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

10. In the **Type** field, select either **New**, **Update**, **Delete** or **Local Save**.

    **Note:** The **Local Save** option relates only to offline steps. The option is used to save input form data locally on the user's device when users perform either a Save or Submit action.

11. Select the associated attachments to current record field and choose the relevant attachment inputs.

    Attachments added in the input form are linked to the record when the write-back action step is triggered by a Save or Submit action. For more information, see [Associate input form attachments to the activity stream in offline](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/input-form-attach-activity-stream.md).

12. Complete the rest of the form as required.

13. Select **Submit**.


**Parent Topic:**[Using action items and action item steps in ofﬂine mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/offline-action-item-steps.md)

