---
title: Review event details and start an exercise event
description: Review the details of an event in the Details tab, start an event to test your business continuity or recovery plan, and monitor completion of the event.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Structured workflows for Exercise and Crisis Management, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Review event details and start an exercise event

Review the details of an event in the **Details** tab, start an event to test your business continuity or recovery plan, and monitor completion of the event.

## Before you begin

Role required: sn\_bcm.planner, sn\_bcm.program\_manager

## Procedure

1.  Navigate to **Business Continuity** &gt; **Business Continuity Workspace**.

2.  Click the lists icon \(![Lists icon.](../../grc-workspace-audit/image/ListsIcon.jpg)\).

3.  Click the **Pending** state in the Exercises list.

4.  Click the link to the event record in the **Number** column.

5.  Review the exercise event details in the **Details** tab and update if required.

<table id="table_lv2_hcq_cnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Event

</td></tr><tr><td>

Short description

</td><td>

Brief description about the event.

</td></tr><tr><td>

Event Type

</td><td>

Auto-populates the event type

</td></tr><tr><td>

State

</td><td>

Current status of the event.

</td></tr><tr><td>

Assigned to

</td><td>

Event coordinator to manage and complete the event.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the event.

</td></tr><tr><td class="sub-head" colspan="2">

Planning

</td></tr><tr><td>

Planned Start

</td><td>

Planned start date of the event.

</td></tr><tr><td>

Plan Approvers

</td><td>

Approvers of the event exercise.

</td></tr><tr><td>

Result Approvers

</td><td>

Person who approves the result of the plan.

</td></tr><tr><td class="sub-head" colspan="2">

Scope

</td></tr><tr><td>

Exercise Method

</td><td>

Method to implement the event. Autopopulates the exercise method previously selected.

</td></tr><tr><td>

Goals

</td><td>

Goals to achieve from the exercise event.

</td></tr><tr><td>

Objectives

</td><td>

Objective of the event.

</td></tr><tr><td class="sub-head" colspan="2">

Results

</td></tr><tr><td>

Actual start

</td><td>

Actual start date of the exercise.

</td></tr><tr><td>

Actual end

</td><td>

Date on which the exercise was completed.

</td></tr><tr><td>

Closed on

</td><td>

Date on which the exercise event was closed.The field appears when the event is moved to closed state.

</td></tr><tr><td>

Result

</td><td>

Outcome of the exercise.

</td></tr><tr><td>

Result Summary

</td><td>

Summary of the exercise event.

</td></tr><tr><td>

Recommended Improvements

</td><td>

Recommendations on how to improve the exercise event.

</td></tr><tr><td class="sub-head" colspan="2">

Activity

</td></tr><tr><td>

Work notes

</td><td>

Additional information about the exercise event.

</td></tr></tbody>
</table>    **Note:** You cannot view the **Results** section in **Pending** state. However, you can view the section in all other states.

6.  Click **Save**.

    The event is in **Pending** state.

7.  Click **Start event** for the exercise after you have updated the details.

    When you start an exercise, the **State** field moves to **Work in Progress** state. As a result approver, you can update the actual start and end dates of the exercise if the exercise was not conducted on the planned date. Update the outcome or the result of the exercise. The result can be Successful, Successful with Issues, or Unsuccessful. Enter the result summary and recommended improvements that can be followed for future exercises.

8.  If all the activated plans of the event tasks for the exercise event are completed, click the **Submit for Approval** button.

    You must enter the **Actual start** and **Actual end** dates before submitting the exercise event for approval. Update the details in the **Results** section. Save the form after you make the changes and before submitting it for approval.

    -   **Pending Approval**

        When you click **Submit for Approval**, the event is set to **Pending Approval** state. In this state, you can only update the **Work notes** field. If there are any approval rules configured for the event, then approvals are generated and sent to the approvers. If there are no approval records in the requested state for the event, then you can either **Reject** or **Approve** the event.

        You can view the approval details in the Approvals related list with its name, level of approval, and the state of the approval.

        Select the Approval History related list to view the approval state, name of the approver, event number, the date on which the approval was requested, and comments if any.

        **Note:** If you are a BCM Program Manager, then you can see the **Approve** and **Reject** buttons.

    -   **Returned**

        When the event is rejected, the state is set to **Returned** state. It can be moved to **Submit for Approval**, **Closed Complete** or **Closed Incomplete** states. Since this is related to an event, only certain sections like description, results, and work notes can be updated in the form.

        When the event is in **Returned** state, you can edit the state of the event asset.

        From the **Returned** state onwards, you can only add comments and attachments to the event task.

    -   **Closed Complete and Closed Incomplete**

        You can set the event state to either **Closed Complete** or **Closed Incomplete** by clicking the **Close Event** button.

    -   **Approved**

        When the event is approved, the state is set to **Approved** state. You can set the event state to either **Closed Complete** or **Closed Incomplete**.

9.  To generate a PDF, click **Generate PDF** button and download the PDF.

    If you have edit access to the exercise event, you can save a copy of the event in PDF format to your local hard drive.

    **Note:** By default, the PDF is generated and attached after the event is closed.


