---
title: Modify CAB meeting details
description: Modify the agenda items for a specific Change Advisory Board \(CAB\) meeting.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/refresh-cab-meeting-agenda-items.html
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Create a single CAB meeting occurrence, Working with the CAB Workbench, Use, Change Management, IT Service Management]
---

# Modify CAB meeting details

Modify the agenda items for a specific Change Advisory Board \(CAB\) meeting.

## Before you begin

Role required: itil, sn\_change\_read, sn\_change\_write, or sn\_change\_cab.cab\_manager

## About this task

After you update the CAB board or change request conditions, refresh the CAB meeting to apply the updates. If you add new board members or attendees to the meeting, they are notified by email invitation after the meeting is refreshed.

**Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/service-operations-workspace/redirect-ui16-module-links-sow.md).

## Procedure

1.  Navigate to the CAB meeting whose agenda you want to modify.

<table id="choicetable_mh3_bkv_lz"><tbody><tr><td id="d190134e93">

**Open from the CAB meeting list**

</td><td>

1.  Navigate to **Change** &gt; **Change Advisory Board** &gt; **All CAB meetings**.
2.  Select and open the CAB meeting to modify.


</td></tr><tr><td id="d190134e123">

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

Condition builder to specify which change requests are added to the CAB meeting agenda.-   **Add Filter Condition**: Select to add more filter conditions, or select **AND** next to the existing filter condition.
-   **Add “OR” Clause**: Select to display the results of multiple filter criteria in a single list.
-   **Add Sort**: Select to define the order of the change requests in this CAB meeting agenda. The agenda order can be defined in CAB Definitions or CAB Meetings, and can be based on one or more fields.


</td></tr><tr><td>

Time per Agenda Item

</td><td>

The time, in minutes and seconds, allotted to discuss each change request on the agenda. The allotted time can be adjusted for agenda items before or during the meeting.

</td></tr><tr><td>

Complete Pre-approved Changes

</td><td>

Check box to mark each pre-approved change request as **Complete** in the CAB meeting agenda. **Note:** Pre-approved changes are automatically marked as complete so that approvers do not have to review them. The pre-approved changes are visible in the CAB Workbench, and can be discussed if necessary.

</td></tr></tbody>
</table>3.  Under **Related Links**, select any of the following links as needed.

    |Link|Description|
    |----|-----------|
    |Refresh Agenda Items|The agenda items for the CAB meeting are refreshed. If you added or updated attendees, a confirmation message asks if the meeting request must be resent to these attendees.|
    |Send meeting request to attendees|Link that resends the meeting request to the list of attendees.|
    |Go to this meeting in CAB Workbench|Link that opens the meeting in CAB Workbench. This link is available only when it is time for the CAB to begin.|
    |Share notes|Share notes captured in the **Meeting Notes** field to the list of meeting attendees. **Share Notes** is visible only when the meeting is **In Progress** or **Complete**.|

4.  In the related lists, do any of the following tasks as needed.

    |Related list|Description|
    |------------|-----------|
    |Agenda Items|Manually add agenda items. In the **Allotted Time** field, the CAB manager can override the default time for any agenda item.|
    |Attendees|Manually add attendees to a CAB meeting.|

5.  Select **Update** to save your changes.


**Parent Topic:**[Create a single CAB meeting occurrence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/create-a-cab-meeting.md)

**Related topics**  


[OR conditions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_UsingORConditions.md)

