---
title: Modify CAB meeting details
description: You can modify the agenda items for a specific CAB meeting.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Create a single CAB meeting occurrence, Working with the CAB Workbench, Using Change Management, Change Management, IT Service Management]
---

# Modify CAB meeting details

You can modify the agenda items for a specific CAB meeting.

## Before you begin

Role required: itil, sn\_change\_read, sn\_change\_write, or sn\_change\_cab.cab\_manager

## About this task

After you update the CAB board or change request conditions, refresh the CAB meeting to apply the updates. If you add new board members or attendees to the meeting, they are notified via email invitations after the meeting is refreshed.

## Procedure

1.  Navigate to the CAB meeting whose agenda you want to modify using one of the following steps.

<table id="choicetable_mh3_bkv_lz"><tbody><tr><td id="d322716e62">

**Open from the CAB meeting list**

</td><td>

1.  Navigate to **Change** &gt; **Change Advisory Board** &gt; **All CAB meetings**.
2.  Select and open the CAB meeting to modify.


</td></tr><tr><td id="d322716e92">

**Open from the CAB definition list**

</td><td>

1.  Navigate to **Change** &gt; **Change Advisory Board** &gt; **All CAB definitions**.
2.  Select and open the CAB definition to send out the meeting request.
3.  Select and open the specific CAB meeting to modify.


</td></tr></tbody>
</table>2.  Modify the CAB meeting agenda in the **Agenda Management** tab or form section, as appropriate.

<table id="table_umf_xhf_jx"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Notification lead time

</td><td>

The advanced notification on the number of agenda items that needs to be discussed.

</td></tr><tr><td>

Automatically Add Change Requests

</td><td>

Check box to define the types of change requests that are automatically added to the CAB meeting agenda. When you select **Automatically Add Change Requests**, the **Refresh CAB Meetings** related link appears. If you click this link, search is performed for change requests that match the value in the **Change Request Addition Conditions** field. If there are any matching change requests, agenda items are created for them and added to the CAB agenda.

 If you do not select **Automatically Add Change Requests**, then you need to create each agenda item for the associated change request for the meeting agenda.

</td></tr><tr><td>

Change Request Addition Conditions

</td><td>

Condition builder to specify which change requests are added to the CAB meeting agenda.-   **Add Filter Condition**: Click to add additional filter conditions, or click **AND** next to the existing filter condition.
-   **Add “OR” Clause**: Click to display the results of multiple filter criteria in a single list.
-   **Add Sort**: Click to define the order of the change requests in this CAB meeting agenda. The agenda order can be defined in CAB Definitions or CAB Meetings, and can be based on one or more fields.


</td></tr><tr><td>

Time per Agenda Item

</td><td>

The time, in minutes and seconds, allotted to discuss each change request on the agenda. The allotted time can be adjusted for agenda items before or during the meeting.

</td></tr><tr><td>

Complete Pre-approved Changes

</td><td>

Check box to mark each pre-approved change request as **Complete** in the CAB meeting agenda. **Note:** Pre-approved changes are automatically marked as complete so that approvers do not have to review them. The pre-approved changes are visible in the CAB Workbench, and can be discussed if necessary.

</td></tr></tbody>
</table>3.  From **Related Links**, you can perform any of the following tasks.

    |Link|Description|
    |----|-----------|
    |Refresh Agenda Items|The agenda items for the CAB meeting are refreshed. If you added or updated attendees, a confirmation message asks if the meeting request must be resent to these attendees.|
    |Send meeting request to attendees|Click to manually resend the meeting request to the list of attendees.|
    |Go to this meeting in CAB Workbench|Click to open the meeting in the CAB workbench. This link is available only when it is time for the CAB to begin.|
    |Share notes|Share notes captured in the **Meeting Notes** field to the list of meeting attendees. **Share Notes** is only visible when the meeting is **In Progress** or **Complete**.|

4.  From related lists, you can perform any of the following tasks.

    |Related list|Description|
    |------------|-----------|
    |Agenda Items|Manually add agenda items. In the **Allotted Time** field, the CAB manager can override the default time for any agenda item.|
    |Attendees|Manually add attendees to a CAB meeting.|

5.  Click **Update** to save your changes.


**Parent Topic:**[Create a single CAB meeting occurrence](create-a-cab-meeting.md)

**Related topics**  


[OR conditions](https://www.servicenow.com/docs/access?context=c_UsingORConditions&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)

