---
title: Create change requests for AI assets
description: Create a change request to modify the relationships between a deployed AI asset and its related assets.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Creating requests for AI assets, Use, AI Control Tower, Enable AI experiences]
---

# Create change requests for AI assets

Create a change request to modify the relationships between a deployed AI asset and its related assets.

## Before you begin

Role required:

-   AI steward \(sn\_ai\_governance\_ai\_steward\)
-   AI asset owner \(sn\_ai\_asset\_mgmt.ai\_asset\_owner\)

## About this task

To modify the relationships between related AI assets, a user with the AI asset owner \(sn\_ai\_asset\_mgmt.ai\_asset\_owner\) role can initiate the change process by creating and submitting a change request. After the request is submitted, a user with the AI steward \(sn\_ai\_governance\_ai\_steward\) role can review and approve the request. This approval triggers the AI Control Tower application to create a new AI asset record for the asset that the change request was created for. The asset then automatically enters the onboarding stage of the asset life cycle.

You can create change requests for the following AI asset types:

-   AI systems \(classic, generative, and agentic\)
-   AI models
-   Datasets

## Procedure

1.  Navigate to **Workspaces** &gt; **AI Control Tower**.

2.  If you have the AI asset owner \(sn\_ai\_asset\_mgmt.ai\_asset\_owner\) role, create a change request.

    1.  Initiate the request by using one of the following navigation options.

<table id="table_tsq_c2x_g3c"><thead><tr><th>

Navigation option

</th><th>

Procedure

</th></tr></thead><tbody><tr><td>

AI Control Tower Home view

</td><td>

1.  From the Home view of the AI Control Tower workspace, select the **Create request** drop-down menu.
2.  Select **Create a change request**.


</td></tr><tr><td>

Change requests list

</td><td>

1.  From the AI Control Tower workspace, open the AI assets view.
2.  From the navigation menu of the AI assets view, navigate to **Requests** &gt; **Change requests**.
3.  Select **Create change request**.


</td></tr><tr><td>

AI asset record

</td><td>

1.  From the AI Control Tower workspace, open the AI assets view.
2.  From the navigation menu of the AI assets view, locate the **AI asset inventory - Managed** section and then select the subsection for the type of AI asset that you want to create a change request for.

Alternatively, navigate to **Lifecycle** &gt; **Deploy**.

3.  Select an AI asset that meets the following criteria:
    -   The State is set to Deployed.
    -   The Lifecycle phase is set to Deploy.
    -   The Lifecycle status is set to Deployed.
4.  Select the **Create a request** drop-down menu.
5.  Select **Create a change request**.


</td></tr></tbody>
</table>    2.  On the form, fill in the fields.

<table id="table_mbs_bzw_g3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Change details

</td></tr><tr><td>

Asset in review

</td><td>

The AI Asset that you want to modify related asset relationships for.**Note:** If you initiated the change request from an AI asset record, this field populates automatically.

</td></tr><tr><td>

Version

</td><td>

Updated version number of the AI asset.

</td></tr><tr><td>

Due date

</td><td>

Date and time at which the request must be completed.

</td></tr><tr><td>

Justification

</td><td>

Justification for creating the request.

</td></tr><tr><td colspan="2">

Sub AI systems**Note:** This form section appears only if you are creating a change request for an AI system with an Asset type of either Generative AI or Agentic AI.

</td></tr><tr><td>

Updated Sub AI systems

</td><td>

Related AI components or subsystems that you want to associate the AI asset with.

</td></tr><tr><td colspan="2">

AI models**Note:** This form section appears only if you are creating a change request for an AI system.

</td></tr><tr><td>

Updated models

</td><td>

Related AI models that you want to associate the AI asset with.

</td></tr><tr><td colspan="2">

AI prompts**Note:** This form section appears only if you are creating a change request for an AI system.

</td></tr><tr><td>

Updated prompts

</td><td>

Related prompts that you want to associate the AI asset with.

</td></tr><tr><td colspan="2">

Evaluation dataset**Note:** This form section appears only if you are creating a change request for an AI system or AI model.

</td></tr><tr><td>

Updated evaluation datasets

</td><td>

Related evaluation datasets that you want to associate the AI asset with.

</td></tr><tr><td colspan="2">

Tools**Note:** This form section appears only if you are creating a change request for an agentic AI system.

</td></tr><tr><td>

Updated tools

</td><td>

Related tools that you want to associate the AI asset with.

</td></tr><tr><td colspan="2">

Training datasets**Note:** This form section appears only if you are creating a change request for an AI model.

</td></tr><tr><td>

Updated training datasets

</td><td>

Related training datasets that you want to associate the AI asset with.

</td></tr><tr><td colspan="2">

Source**Note:** This form section appears only if you are creating a change request for a dataset.

</td></tr><tr><td>

Updated source

</td><td>

Related data source that you want to associate the AI asset with.

</td></tr><tr><td colspan="2">

Base datasets**Note:** This form section appears only if you are creating a change request for a dataset.

</td></tr><tr><td>

Updated base datasets

</td><td>

Related base dataset that you want to associate the AI asset with.

</td></tr><tr><td colspan="2">

Dataset card**Note:** This form section appears only if you are creating a change request for a dataset.

</td></tr><tr><td>

Updated dataset card

</td><td>

Related dataset card that you want to associate the AI asset with.

</td></tr></tbody>
</table>    3.  Select **Submit for review**.

    4.  In the Submit change request dialog box, select **Submit request**.

        After the dialog box closes, you are automatically redirected to the new change request record.

3.  If you have the AI steward \(sn\_ai\_governance\_ai\_steward\) role, approve or reject the request.

    1.  Open the change request record by using one of the following navigation options.

<table id="table_s2l_ghx_g3c"><thead><tr><th>

Navigation option

</th><th>

Procedure

</th></tr></thead><tbody><tr><td>

Change requests list

</td><td>

1.  From the AI Control Tower workspace, open the AI assets view.
2.  From the navigation menu of the AI assets view, navigate to **Requests** &gt; **Change requests**.
3.  From the list of available change requests, select the record number for the request that you want to approve.


</td></tr><tr><td>

AI asset record

</td><td>

1.  From the AI Control Tower workspace, open the AI assets view.
2.  From the navigation menu of the AI assets view, locate the **AI asset inventory - Managed** section and then select the subsection for the type of AI asset that the change request was created for.

Alternatively, navigate to **Lifecycle** &gt; **Deploy**.

3.  Select the AI asset that the change request was created for.
4.  On the AI asset record, select the **Requests** tab.
5.  Select **Change requests** from the request types menu.
6.  From the list of available change requests, select the record number for the request that you want to approve.


</td></tr></tbody>
</table>        The change request record opens.

    2.  On the **Details** tab, set the **Assigned to** field to the user who you want to assign the change request to.

        You can assign the request to yourself or to any other user with the AI steward \(sn\_ai\_governance\_ai\_steward\) role.

    3.  If you are the assigned user, approve or reject the request.

        -   To approve the request, select **Approve**.
        -   To reject the request, select **Reject**.
    -   If you approved the request, the Status changes to Approved and the State changes to In progress.

        The AI Control Tower application then generates a change task for each asset that is impacted by the request. These change tasks appear on the **Change tasks** tab and specify the actions that must be taken on the impacted assets. Each change task is assigned to a user with the AI asset owner \(sn\_ai\_asset\_mgmt.ai\_asset\_owner\) role. If you have any concerns or need further clarification on the request, you can create additional change tasks manually. After the assigned users complete all change tasks, the AI Control Tower application automatically creates a new AI asset record for the asset that the change request was created for. The State of the request then changes to Completed.

        **Note:** The **Change tasks** tab is not available if the change request was created for a dataset.

    -   If you rejected the request, the Status changes to Rejected and the State changes to Completed.

