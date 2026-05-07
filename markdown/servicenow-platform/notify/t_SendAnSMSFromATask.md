---
title: Send an SMS alert from a task
description: Use Notify to send information related to a call through SMS alerts from a task record.
locale: en-US
release: australia
product: Notify
classification: notify
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Notify with tasks, Using Notify, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Send an SMS alert from a task

Use Notify to send information related to a call through SMS alerts from a task record.

## Before you begin

Role required: notify\_view, or itil

## About this task

Ensure that there are Notify phone numbers \(E.164 or short code\) in number groups with SMS workflows.

Use **glide.enable.notify\_on\_task** property to enable Notify integration for Task table and its extensions. Entering phone number in **glide.notify.task.phone\_number** property is equivalent to setting **glide.enable.notify\_on\_task** to true.

## Procedure

1.  Navigate to any task record such as an incident or a change request.

2.  Click the **Send SMS** related link.

3.  In the **From** choice list, select the phone number from which you want to send the SMS message.

4.  Select and add the participants to whom you want to send the SMS message.

    All users from the **User Contacts** list in the incident communication plan are in the Recommended section by default.

    The dialog box displays the Recommended and Selected participants you selected to send an SMS message.

5.  To select ad-hoc participants, choose one of the following actions.

<table id="choicetable_b2f_p4c_lq"><tbody><tr><td id="d84637e143">

**Click the reference lookup icon and select the relevant user**

</td><td>

Click **Add to selected**.

</td></tr><tr><td id="d84637e155">

**Enter the participant's phone number**

</td><td>

Click **Add to selected**.

</td></tr></tbody>
</table>6.  After the participant list is finalized, type the message you want to send to the participants in the **Message** field and click **Send SMS**.


## Result

Any SMS records created from a task are associated with that task. You can view associated SMS messages from the task record in the **SMS Messages** related list. You might need to configure the form to add this related list.

**Parent Topic:**[Using Notify with tasks](../concept/c_NotifyOnTask.md)

**Related topics**  


[Start a conference call from a task](t_StartAConferenceCallFromATask.md)

[Manage conference calls on task](manage-conf-call.md)

