---
title: Conduct a CAB meeting in the CAB workbench
description: Start and conduct a Change Advisory Board meeting in the CAB Workbench in Service Operations Workspace to review the agenda and approve or schedule changes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-operations-workspace/cm-manage-cab-meeting-workbench-sow.html
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [CAB in Service Operations Workspace, CAB Workbench in Service Operations Workspace]
breadcrumb: [Change Management in Service Operations Workspace, Operating IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# Conduct a CAB meeting in the CAB workbench

Start and conduct a Change Advisory Board meeting in the CAB Workbench in Service Operations Workspace to review the agenda and approve or schedule changes.

## Before you begin

Role required: sn\_change\_cab.cab\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  Select the List icon \(\[Omitted image "sow-list.png"\] Alt text: List icon.\).

3.  In the **Change Advisory Board** tab, select **My upcoming CAB meetings**.

4.  Open a CAB meeting.

5.  Select **Open in CAB Workbench**.

    The CAB meeting opens in the CAB Workbench.

    \[Omitted image "cm-cab-workbench-meeting-sow.png"\] Alt text: CAB workbench shows a CAB meeting in progress, and an agenda item with its details.

6.  Select **Start meeting** to start the meeting.

    Each attendee who connects to the meeting has independent access to the widgets on the meeting page on the CAB workbench while the meeting is in progress.

7.  Review the agenda items, and approve or reject them.

    1.  Select the agenda item to see its details.

        **Note:** The timer displays the time remaining for discussing the current meeting agenda item. The color code in the timer changes based on the overall percentage of time elapsed from the total duration of the meeting.

        -   Green: 0% - 50%
        -   Yellow: 50% - 70%
        -   Orange: 75% - 100%:
        -   Red: &lt; 100%:
    2.  Select the change request number either from the agenda item card or form header of its details to open the change request record.

    3.  Review the details of the change for any scheduling conflicts such as another change or a blackout or holiday schedule.

    4.  After reviewing and discussing, any assigned approver for the related change request can approve or reject.

        1.  Select **Make approval decision**.

            **Note:** The button is available only to change approvers.

        2.  In the Approval decision dialog box, select **Approve** to approve or **Reject** to reject the agenda item.
        3.  Add comments about the decision in **Approval notes**.
        4.  Select **Submit**.
        CAB manager or approvers' decisions on agenda items—whether approved, rejected, or skipped without any decision—are automatically noted in the meeting notes. These decisions are also saved in the **Meeting notes** field of the related CAB meeting record. The timer for the agenda item stops and the agenda item is moved to the **All** tab.

    5.  Select **Pause** to pause the timer of the current agenda item.

    6.  Select **Resume** to resume the timer of the current agenda item.

    7.  Select **Next item** if you want to skip an agenda item.

        **Note:** The current agenda item is moved as the last card in the **Up next** tab. The next agenda item in the list displays.

    8.  In the **Up next** tab, select the second or any subsequent agenda item to move it to the top of the list by selecting **Make next agenda item**.

    9.  In the **Deferred** tab, view the deferred agenda items and select an agenda item and select **Restore** to restore them for discussion.

        The agenda item moves to the **Up next** tab.

    10. In the **All** tab, view agenda items by using the filters: All agenda Items, My agenda items, and Completed.

8.  In the contextual menu, view the meeting details, attendees list, and take meeting notes.

    -   Select the meeting information icon \(\[Omitted image "cm-icon-meeting-info.png"\] Alt text: Meeting information icon.\) to view the meeting details.
    -   Select the attendees icon \(\[Omitted image "cm-icon-attendee.png"\] Alt text: Attendees icon.\) to view the list of attendees along with their response to the meeting invitation.

        The green circle mark next to the name of attendees indicates they are currently connected to the meeting.

    -   Select the notes icon \(\[Omitted image "cm-icon-meeting-notes.png"\] Alt text: Notes icon.\) to enter meeting notes and save into the CAB meeting record or email it to the attendees.

        **Note:** Only the CAB manager or delegates can enter the notes for the overall meeting. Other attendees in the meeting can review the notes in the read-only mode.

9.  After all agenda items have been reviewed, select **End Meeting** to end the CAB meeting.


## Result

-   The CAB meeting ends and its state is updated to Complete.
-   In the CAB meeting record, the following fields are updated:
    -   **Meeting end time**: Shows when the meeting ended.
    -   **Meeting notes**: Shows notes taken during the meeting and decision comments on agenda items.

**Parent Topic:**[Change Management in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/change-sow.md)

**Related topics**  


[Create a change request in Service Operations Workspace]()

[Work on a change request in Service Operations Workspace]()

[Standard change catalog]()

[Create a change task in Service Operations Workspace]()

[Work on a change task in Service Operations Workspace]()

[Create a Change Advisory Board \(CAB\) definition]()

[Create a CAB meeting]()

