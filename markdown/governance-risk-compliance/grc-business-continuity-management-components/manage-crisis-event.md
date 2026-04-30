---
title: Manage a crisis event
description: Review and update the details of a crisis event in the Details tab. Get the event ready for a crisis that may strike and disrupt your business.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Structured workflows for Exercise and Crisis Management, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Manage a crisis event

Review and update the details of a crisis event in the **Details** tab. Get the event ready for a crisis that may strike and disrupt your business.

## Before you begin

Role required: sn\_bcm.planner, sn\_bcm.program\_manager

## Procedure

1.  Navigate to **Business Continuity** &gt; **Business Continuity Workspace**.

2.  Click the lists icon \(![Lists icon](../../grc-workspace-audit/image/ListsIcon.jpg)\).

3.  Click **Pending** state in the Crisis Events list.

4.  Click the link to the event record in the **Number** column.

5.  Review the crisis event details and update if required.

<table id="table_lv2_hcq_cnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Event

</td></tr><tr><td>

Short description

</td><td>

Name or description of the event.

</td></tr><tr><td>

Event Type

</td><td>

Autopopulates the event type

</td></tr><tr><td>

State

</td><td>

Current status of the event.

</td></tr><tr><td>

Assigned to

</td><td>

Event coordinator who manages the crisis.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the event.

</td></tr><tr><td class="sub-head" colspan="2">

Additional Information

</td></tr><tr><td>

Actual start

</td><td>

Actual start date of the crisis event.

</td></tr><tr><td>

Actual end

</td><td>

Date on which the crisis event ended.

</td></tr><tr><td>

Closed on

</td><td>

Date on which the event was closed.The field appears when the event is moved to closed state.

</td></tr><tr><td class="sub-head" colspan="2">

Activity

</td></tr><tr><td>

Work notes

</td><td>

Additional information about the crisis event.

</td></tr><tr><td class="sub-head" colspan="2">

Compose

</td></tr><tr><td>

Work notes \(Private\)

</td><td>

Additional information about the crisis event.

</td></tr></tbody>
</table>6.  Click the **Browse** button to add any document as an attachment.

7.  Click **Save**.

    The event is in **Pending** state.

8.  To start the crisis event, click **Start Event** button.

    After you start the event, it moves to **Work in Progress** state.

9.  If all the activated plans of the event tasks for the crisis event are completed, click **Submit for Approval** button.

    You must enter the **Actual end** date and save the form before submitting the event for approval.

    -   **Pending Approval**

        When you click **Submit for Approval**, the event is set to **Pending Approval** state. In this state, you can only update the **Work notes** field.

        If there are any approval rules configured for the event, then approvals are generated and sent to the approvers. If there are no approval records in the requested state for the event, then you can either **Reject** or **Approve** the event.

        You can view the approval details in the Approvals related list with its name, level of approval, and the state of the approval.

        Select the Approval History related list to view the approval state, name of the approver, event number, the date on which the approval was requested, and comments if any.

        **Note:** If you are a BCM Program Manager, then you can see the **Approve** and **Reject** buttons.

    -   **Returned**

        When the event is rejected, the state is set to **Returned** state. It can be moved to **Submit for Approval**, **Closed Complete** or **Closed Incomplete** states. Since this is related to an event only certain sections like description, results, and work notes can be updated in the form.

        When the event is in **Returned** state, you can edit the state of the event asset.

        From the **Returned** state onwards, you can only add comments and attachments to the event task.

    -   **Closed Complete and Closed Incomplete**

        When the event is approved, the only option available is to close the event. You can set the event state to either **Closed Complete** or **Closed Incomplete** by clicking the **Close Event** button.

    -   **Approved**

        When the event is approved, the state is set to **Approved** state. You can set the event state to either **Closed Complete** or **Closed Incomplete**.

10. To generate a PDF, click **Generate PDF** button and download the PDF.

    If you have edit access to the crisis event, you can save a copy of the event in PDF format to your local hard drive.

    **Note:** By default, the PDF is generated and attached after the event is closed.


**Parent Topic:**[Structured workflows for Exercise and Crisis Management](../concept/bcm-recovery-exercise-management.md)

