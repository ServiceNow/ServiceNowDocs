---
title: Approve a localization task
description: Proofread the translated content and approve a localization task.
locale: en-US
release: australia
product: Localization Framework
classification: localization-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create translation projects, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Approve a localization task

Proofread the translated content and approve a localization task.

## Before you begin

Role required: localization\_fulfiller

## Procedure

1.  Navigate to **All** &gt; **Localization Framework** &gt; **My Tasks**.

2.  Select a localization task in the **Open**state.

3.  Select **Translate**.

    A list of all the requested items with the translation status is displayed. You can expand each requested item to see the details.

4.  Select **Submit For Approval**.

    The state of the localization task is changed to **Under Review**. An approval localization task is created and assigned to an approver according to the approver group assigned in localization settings.

5.  Select to open the approval localization task record.

    The state of the approval localization task is set to **Requested**.

6.  From the form header, select **Verify Translations**.

    A list of all the requested items is displayed. Each requested expands to display the comparison UI.

7.  On the form header, select **Approve**.

    All the translations are published and the states of the requested items, localization task, and the localization project is changed to **Closed Complete**.

8.  On the form header, select **Request Changes** if you want to reject the translations.

    The approval localization task state is changed to **Rejected**. The requester needs to create another approval task and assign to the approval group.


