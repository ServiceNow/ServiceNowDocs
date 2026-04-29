---
title: Create offboarding requests for AI assets
description: Create an offboarding request to retire AI assets that are no longer needed.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Creating requests for AI assets, Use, AI Control Tower, Enable AI experiences]
---

# Create offboarding requests for AI assets

Create an offboarding request to retire AI assets that are no longer needed.

## Before you begin

Role required:

-   AI asset owner \(sn\_ai\_asset\_mgmt.ai\_asset\_owner\)
-   AI steward \(sn\_ai\_governance\_ai\_steward\)

## About this task

To retire a deployed AI asset, a user with the AI asset owner \(sn\_ai\_asset\_mgmt.ai\_asset\_owner\) role can initiate the offboarding process by creating and submitting an offboarding request. After the request is submitted, a user with the AI steward \(sn\_ai\_governance\_ai\_steward\) role can review and approves the request. This approval triggers the offboarding workflow that assigns tasks to impacted asset owners and updates the Status of the AI asset record to Retired upon completion.

**Note:** We have automated the ServiceNow AI model to initiate the offboarding workflows when a deprecation date is present.

You can create offboarding requests for the following AI asset types:

-   AI systems \(classic, generative, and agentic\)
-   AI models
-   Datasets
-   MCP servers

## Procedure

1.  Navigate to **Workspaces** &gt; **AI Control Tower**.

2.  If you have the AI asset owner \(sn\_ai\_asset\_mgmt.ai\_asset\_owner\) role, create an offboarding request.

    1.  Initiate the request by using one of the following navigation options.

<table id="table_tsq_c2x_g3c"><thead><tr><th>

Navigation option

</th><th>

Procedure

</th></tr></thead><tbody><tr><td>

AI Control Tower Home view

</td><td>

1.  From the Home view of the AI Control Tower workspace, select the **Create request** drop-down menu.
2.  Select **Create an offboarding request**.


</td></tr><tr><td>

Offboarding requests list

</td><td>

1.  From the AI Control Tower workspace, open the AI assets view.
2.  From the navigation menu of the AI assets view, navigate to **Requests** &gt; **Offboarding requests**.
3.  Select **Create offboarding request**.


</td></tr><tr><td>

AI asset record

</td><td>

1.  From the AI Control Tower workspace, open the AI assets view.
2.  From the navigation menu of the AI assets view, locate the **AI asset inventory - Managed** section and then select the subsection for the type of AI asset that you want to retire.

Alternatively, navigate to **Lifecycle** &gt; **Deploy**.

3.  Select an AI asset that meets the following criteria:
    -   The State is set to Deployed.
    -   The Lifecycle phase is set to Deploy.
    -   The Lifecycle status is set to Deployed.
4.  Select the **Create a request** drop-down menu.
5.  Select **Create an offboarding request**.


</td></tr></tbody>
</table>    2.  On the form, fill in the fields.

<table id="table_cj4_x5x_g3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Asset in review

</td><td>

**Note:** If you initiated the offboarding request from an AI asset record, this field populates automatically.

</td></tr><tr><td>

Due date

</td><td>

Date and time at which the request must be completed.

</td></tr><tr><td>

Justification

</td><td>

Justification for creating the request.

</td></tr></tbody>
</table>    3.  Select **Submit for review**.

    4.  In the Submit offboarding request dialog box, select **Submit request**.

        After the dialog box closes, you are automatically redirected to the new offboarding request record.

3.  If you have the AI steward \(sn\_ai\_governance\_ai\_steward\) role, review the request.

    1.  Open the offboarding request record by using one of the following navigation options.

<table id="table_s2l_ghx_g3c"><thead><tr><th>

Navigation option

</th><th>

Procedure

</th></tr></thead><tbody><tr><td>

Offboarding requests list

</td><td>

1.  From the AI Control Tower workspace, open the AI assets view.
2.  From the navigation menu of the AI assets view, navigate to **Requests** &gt; **Offboarding requests**.
3.  From the list of available offboarding requests, select the record number for the request that you want to review.


</td></tr><tr><td>

AI asset record

</td><td>

1.  From the AI Control Tower workspace, open the AI assets view.
2.  From the navigation menu of the AI assets view, locate the **AI asset inventory - Managed** section and then select the subsection for the type of AI asset that the offboarding request was created for.

Alternatively, navigate to **Lifecycle** &gt; **Deploy**.

3.  Select the AI asset that the offboarding request was created for.
4.  On the AI asset record, select the **Requests** tab.
5.  Select **Offboarding requests** from the request types menu.
6.  From the list of available offboarding requests, select the record number for the request that you want to review.


</td></tr></tbody>
</table>        The offboarding request record opens.

    2.  On the **Details** tab, set the **Assigned to** field to the user who you want to assign the offboarding request to.

        You can assign the request to yourself or to any other user with the AI steward \(sn\_ai\_governance\_ai\_steward\) or AI asset owner \(sn\_ai\_asset\_mgmt.ai\_asset\_owner\) role.

    3.  If you are the assigned user, select **Start review**.

        The **Offboarding workflow** tab appears and then the offboarding workflow initiates. In addition, the **Impacted assets** tab automatically updates with the list of assets that are impacted by the request.

        The offboarding workflow contains the Assess, Pre-offboarding tasks, and Offboard stages. You can create and delete relevant tasks in all three stages. Any tasks that are generated for impacted assets also appear in the corresponding workflow stages.

        **Note:** Each user who is assigned to an impacted asset must complete the corresponding task by either accepting or rejecting it.

        -   If the user accepts the task, the Status task changes to Accepted and the State changes to Completed.
        -   If the user rejects the task, the Status of the task changes to Rejected and the State changes to Completed.
    4.  Complete all tasks in the Assess stage.

    5.  Select **Mark as complete** to move to the Pre-offboarding tasks stage.

    6.  Complete all tasks in the Pre-offboarding tasks stage.

    7.  Select **Mark as complete** to move to the Offboard stage.

    8.  Complete all tasks in the Offboard stage.

    9.  Select **Mark as complete**.

    After all three stages are marked as complete, the Status of the request changes to Approved and the State changes to Completed. The State of the asset then changes to Retired.


