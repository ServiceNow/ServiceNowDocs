---
title: Software installation optimization and removal
description: You can optimize your environment by reclaiming unused software as well as removing unauthorized software.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Software installation optimization and removal

You can optimize your environment by reclaiming unused software as well as removing unauthorized software.

If a user is not using software installed, or infrequently, that software can be a candidate for removal. Removal means uninstalling and reallocating the software to an individual who will use it more often. Removal candidates are used to reclaim software installations.

## Overview of software reclamation

Software reclamation is integrated with Workflow and [Client Software Distribution](https://www.servicenow.com/docs/access?context=c_ClientSoftwareDistribution&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) \(CSD\) to automate the process of uninstalling software from devices and reclaiming those software rights. During the workflow, the state of the removal candidate changes based on the progression within the workflow.

**Note:** If you change a software asset's state to **Retired** or **Missing**, the installation associated to the software asset gets removed and a removal candidate won't be created.

Reclamation can be performed for suite based products and for individual products that are not part of a suite.

For suite based products, bulk reclamation is performed at the user level. One removal candidate is created for reclaiming the suite. You can add the suite components to the same removal candidate via the Software Installation related list on the removal candidate form. The potential savings displayed is for the entire suite. Suite components cannot be reclaimed individually. In the Software Asset Workspace, you can add the suite components to the removal candidate one at a time. In the Software Asset Management classic framework, you can add the suite components all at one go.

For individual products, you can specify the software installation that you wish to reclaim.

There are multiple ways that removal candidates get created. A monthly scheduled job, **SAM – Identify new reclamation candidates**, uses the reclamation rules and software usage to create removal candidates. Additionally, removal candidates are also created as part of using remediation options for unlicensed and unallocated software installations, and for restricted software. When a software model is marked as restricted, removal candidates are created for any software associated to that software model. The reclamation flow and process is the same in all these use cases.

The **SAM – Identify new reclamation candidates** scheduled job creates removal candidates and these removal candidates automatically have the bulk reclamation flag checked. The removal candidates created are based on the results from the reconciliation process. Verify that at least one reconciliation process has run with successful results before running the **SAM – Identify new reclamation candidates** scheduled job. This ensures that the **SAM – Identify new reclamation candidates** scheduled job accurately creates removal candidates to identify the right potential savings.

In each list of Removal Candidates, you can select individual records for reclamation \(**Reclaim**\) or **Reclaim All** to reclaim all qualifying removal candidates. Qualifying candidates are those candidates in the Ready state. Once you select **Reclaim** or **Reclaim All**, the workflow to remove the software is initiated.

## Upgrading to Yokohama

When you upgrade to Yokohama and if you have an existing removal candidate in the**Awaiting revocation** state, nothing will be done with that removal candidate. If that removal candidate was part of a suite, then removal candidates are created for each of the other software installations in that suite. However, if the state of the existing removal candidates is anything other than **Awaiting revocation** then those removal candidates are canceled and a single removal candidate gets created for all the software installations that are part of that suite. In the **Activity** section on the removal candidate form, a reason is mentioned for the closure of each removal candidate.

## Removal candidate grouping

Removal candidates are grouped according to justification.

-   Low Usage
-   Restricted Software
-   All other justifications \( such as Unlicensed, Unallocated\)

<table id="table_xrr_gfs_dbb"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Attention Required

</td><td>

A removal candidate requires attention if the **User** field is empty on an automatic removal candidate that has the **Notify User** check box selected.Once the **User** field is populated, the state automatically changes to Ready.

</td></tr><tr><td>

Ready

</td><td>

When a removal candidate is in the Ready state, you can select **Reclaim** to advance the workflow.

</td></tr><tr><td>

Awaiting User

</td><td>

If the **Notify User** check box was selected, the user was sent a notification of the removal candidate to approve or deny.

</td></tr><tr><td>

Awaiting Approval

</td><td>

If the **Notify User** check box was selected, the user can approve or deny the removal candidate. If the user still wants to keep the software installation, it becomes the responsibility of a member of the assignment group to approve or decline the removal.

</td></tr><tr><td>

Awaiting Revocation

</td><td>

The final step in the workflow. You can select **Close Complete** to reclaim software rights in the removal candidate manually. Otherwise, a weekly scheduled job \(named SAM — Updating Existing Reclamation Candidates\) automatically updates removal candidates in the **Awaiting Revocation** state and with the software install field empty to **Closed Complete** state.

 If the removal candidate is in any other state and the software install is empty, the Reclamation workflow is canceled and updated to **Closed Skipped** state.

 The state for a removal candidate that has restricted software is automatically set to **Awaiting Revocation** and the justification is set to **Restricted Software**.

</td></tr><tr><td>

Closed Complete

</td><td>

Software rights have been reclaimed.

</td></tr><tr><td>

Closed Skipped

</td><td>

Software rights not reclaimed by the removal candidate.

</td></tr><tr><td>

Closed Canceled

</td><td>

Software rights not reclaimed by the removal candidate as user activity is detected.

</td></tr></tbody>
</table>## Restricted software justification and unlicensed justification

Workflows for removal candidates with a restricted software justification or an unlicensed justification get executed automatically. The user is notified of unauthorized software use and is not prompted for approval.

-   Restricted Software:

    `Unauthorized Software Use`

    `[Publisher] [Product] installed on the device, [device name], is not authorized to be used on company property. Do not install this software again.`

-   Unlicensed:

    `Unauthorized Software Use`

    `You are not licensed to use [Publisher] [Product] installed on the device, [device name]. Use the appropriate process to request a license for the software.`


The workflow state for a Restricted software justification and an unlicensed justification is then set to Awaiting Revocation and, once discovery identifies that the installation no longer exists, the state is changed to Closed Complete.

## Unallocated justification and Low Usage justification

Workflows for removal candidates with an unallocated justification or a low usage justification prompt the user for approval.

-   Unallocated:

    `[Publisher] [Product] installed on the device, [device name], has been flagged for removal because an allocation to use the software does not exist. Do you still require access to this software?`

-   Low Usage:

    `[Publisher] [Product] has been flagged for reclamation. Do you still need this software installed on [device name]?`


## Justification descriptions

Removal candidate descriptions get updated based on the justification.

-   Unallocated:

    `[Publisher] [Product] installed on the device, [device name], has been flagged for removal because an allocation to use the software does not exist. If you do not require this software, Reject this task. If you still require access to this software, Approve this task and your request for continued use of the software will be routed for software manager approval.`

-   Unlicensed:

    `[Publisher] [Product] installed on the device, [device name], has been flagged for removal because the licenses to use it are not owned. Please request access to this software through the appropriate process.`

-   Restricted Software:

    `[Publisher] [Product] installed on the device, [device name], is not authorized for use on company owned property.`

-   Low Usage:

    `[Publisher] [Product] installed on the device, [device name], has been flagged for reclamation due to low usage. If you do not require this software, Reject this task. If you still require access to this software, Approve this task and your request for continued use of the software will be routed for manager approval.`


When the **Reclaim** action is clicked, if the **Notify User** field is selected and the days before reclamation is greater than 0, then the state is set to Awaiting User. Otherwise the state is set to Awaiting Reclamation.

When the state changes to Awaiting User, a notification is sent to the user.

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

**Related topics**  


[View or create software usage](../task/view-sw-usage-workspace.md)

[Reclaim software](../task/reclaiming-software-sam.md)

