---
title: Add attendees to a safety meeting
description: Add users to a safety meeting who need to attend this meeting.
locale: en-US
release: xanadu
product: Health and Safety Core
classification: health-and-safety-core
topic_type: task
last_updated: "2025-04-15"
reading_time_minutes: 1
breadcrumb: [Manage safety meetings, Use, Health and Safety Core, Health and Safety, Employee Service Management]
---

# Add attendees to a safety meeting

Add users to a safety meeting who need to attend this meeting.

## Before you begin

Role required: sn\_ohs\_im.meeting\_manager or sn\_ohs\_im.meeting\_writer

## About this task

Using the **Attendees** tab of a safety meeting, you can keep track of all attendees and absentees for the meeting in the same place.

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  Select the meetings icon \(![safety meetings icon](../image/icon-hs-meetings.png)\).

3.  In the **Meetings** list, select the one that you want to add attendees to.

4.  In the **Attendees** tab, select **Add** or **New** to add attendees for this meeting.

<table id="choicetable_owg_bw1_1fc"><thead><tr><th align="left" id="d551732e112">

Option

</th><th align="left" id="d551732e115">

Steps

</th></tr></thead><tbody><tr><td id="d551732e121">

**To add multiple attendees**

</td><td>

Add users with the Health and Safety profile in your organization who are attending this meeting.1.  Select **Add**.
2.  Select **Filter** and use the condition builder to define conditions to choose users to be added as attendees.
3.  Select users in the list and then select **Add**.
For information on Health and Safety profile, see [Health and Safety user profile](../concept/health-and-safety-user-profile.md).

</td></tr><tr><td id="d551732e167">

**To add an external attendee or a single internal attendee**

</td><td>

1.  Select **New**.
2.  On the form, fill in the fields.

For field descriptions, see [Health and Safety meeting attendee form](../reference/hs-safety-meeting-attendee-form.md).

3.  Select **Save**.


</td></tr></tbody>
</table>
## Result

-   The attendees are listed in the **Attendees** tab of the meeting and are saved in the Health and Safety meeting attendee \[sn\_ohs\_im\_meeting\_attendee\] table.
-   For an attendee internal to your organization, the **Attendee profile** column of this list shows the user's Health and Safety profile.
-   For an external attendee, the **Attendee profile** column of this list is empty.

**Parent Topic:**[Managing safety meetings](../concept/managing-hs-safety-meetings.md)

**Related topics**  


[Log a safety meeting](log-hs-safety-meeting.md)

[Create a meeting minute for a safety meeting](create-meeting-minute-hs-safety-meeting.md)

