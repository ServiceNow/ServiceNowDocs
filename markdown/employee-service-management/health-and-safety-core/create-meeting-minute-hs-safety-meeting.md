---
title: Create a meeting minute for a safety meeting
description: Create a meeting minute for a safety meeting to track discussions and accountability.
locale: en-US
release: yokohama
product: Health and Safety Core
classification: health-and-safety-core
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage safety meetings, Use, Health and Safety Core, Health and Safety, Employee Service Management]
---

# Create a meeting minute for a safety meeting

Create a meeting minute for a safety meeting to track discussions and accountability.

## Before you begin

Verify that the minute taker is added as an attendee to this safety meeting. For information on adding a meeting attendee, see [Add attendees to a safety meeting](add-attendees-safety-meeting.md).

Role required: sn\_ohs\_im.meeting\_minute\_taker

## About this task

You can create multiple meeting minutes for different timestamps of a safety meeting. For each minute record, you can add relevant actions to ensure safety concerns are addressed and contributors remain accountable.

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  Select the meetings icon \(![safety meetings icon](../image/icon-hs-meetings.png)\).

3.  In the **Meetings** list, select the one that you want to create meeting minutes for.

4.  In the **Meeting minutes** tab, select **New**.

5.  On the form, fill in the fields.

<table id="table_csw_gpc_1fc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

Brief description about this meeting minute.

</td></tr><tr><td>

Time stamp

</td><td>

Time of the discussion during the meeting.

</td></tr><tr><td>

Contributors

</td><td>

Attendees involved in this discussion.

</td></tr><tr><td>

Sensitive content

</td><td>

Option to indicate that this meeting minute contains sensitive information. Only a user with the Sensitive meeting content user \[sn\_ohs\_im.sensitive\_meeting\_content\_user\] role can view a meeting minute marked as sensitive.

**Note:** Selecting a meeting minute as sensitive content doesn't mark the entire safety meeting or the other meeting minutes for this meeting as sensitive.

</td></tr><tr><td>

Topic discussed

</td><td>

Description about the topic discussed.

</td></tr></tbody>
</table>6.  Select **Save**.

    The **Actions** tabs appear for this meeting

7.  In the **Actions** tab, assign any actions related to this meeting minute.

    -   To create an action, select **New**.
    -   To associate an action from the existing list of actions for this meeting, select **Add**.
    For field descriptions, see [Health and Safety action form](../reference/hs-action-form.md).


## Result

-   The meeting minute is listed in the **Meeting minutes** tab of the meeting and is saved in the Health and Safety meeting minute \[sn\_ohs\_im\_meeting\_minute\] table.
-   Any action for this meeting minute is listed in the **Actions** tab of the minute record. The action is saved in the Health and Safety m2m meeting minute action \[sn\_ohs\_im\_m2m\_meeting\_minute\_action\] table.

**Parent Topic:**[Managing safety meetings](../concept/managing-hs-safety-meetings.md)

**Related topics**  


[Log a safety meeting](log-hs-safety-meeting.md)

[Add attendees to a safety meeting](add-attendees-safety-meeting.md)

