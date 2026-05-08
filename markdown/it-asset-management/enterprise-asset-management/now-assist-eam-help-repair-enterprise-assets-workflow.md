---
title: Fulfill repair orders by using the help repair enterprise assets agentic workflow
description: You can use the help repair enterprise assets agentic workflow to help you manage and complete the troubleshooting and repair of your defective enterprise assets. The workflow uses a collection of AI agents to automatically generate comprehensive troubleshooting, diagnostics, and repair instructions for these assets. The workflow uses also uses these AI agents to automatically validate, update, and close relevant tasks.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Fulfilling repair orders in the Enterprise Asset Workspace, Manage repair of defective assets in your stockroom in the Enterprise Asset Workspace, Create and manage enterprise asset inventory, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Fulfill repair orders by using the help repair enterprise assets agentic workflow

You can use the help repair enterprise assets agentic workflow to help you manage and complete the troubleshooting and repair of your defective enterprise assets. The workflow uses a collection of AI agents to automatically generate comprehensive troubleshooting, diagnostics, and repair instructions for these assets. The workflow uses also uses these AI agents to automatically validate, update, and close relevant tasks.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see ServiceNow product tiers.

**Important:** This agentic workflow is turned on by default. For more information, see Now Assist skills, agents, and agentic workflows on by default.

## Help repair enterprise assets agentic workflow overview

The help repair enterprise assets agentic workflow helps you manage and complete your enterprise asset troubleshooting and repairs. This workflow provides the following benefits:

-   Streamlines the troubleshooting and repair process.
-   Improves the accuracy and consistency of your troubleshooting and repairs.
-   Increases troubleshooting and repair completion rates.
-   Enhances and simplifies the user experience.

**Important:** You can enable security implementation to execute AI agents and agentic workflows through Access Control Lists \(ACLs\) and user identities. ACLs provide the Run As capability to let agents and agentic workflows execute actions either as a dynamic user or as an AI user. For more information, see Implement access control in Now Assist AI agents.

**Important:** By default, all agentic workflows and AI agent records are read-only.

## Role masking

Agentic workflows and their AI agents use role masking to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see Define security controls for an agentic workflow.

## Validating repair asset tasks

Before the help repair enterprise assets agentic workflow can help you manage and complete the troubleshooting or repair of a defective enterprise asset, it must validate the corresponding repair asset task. The workflow proceeds only if the task meets the following criteria:

-   The task has a valid and unique task number.
-   The task is active.
-   The task has not already been completed.
-   The task is assigned to a user with the sn\_eam.asset\_technician role.
-   The asset is associated with one of the following models:
    -   Any valid enterprise model
    -   Any valid hardware model that is supported by the OT Asset Management application

## Stages in the help repair enterprise assets agentic workflow

The help repair enterprise assets agentic workflow helps you manage and complete the troubleshooting and repair of defective enterprise assets through the following stages.

<table id="table_rbs_4lg_rhc"><thead><tr><th>

Stage

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Enterprise asset repair initiation

</td><td>

1.  A user with the sn\_eam.asset\_technician role requests the repair of a defective enterprise asset through one of the following options:
    -   The Service Catalog application

For more information on this request option, see [Request repair of enterprise assets using Service Catalog](../../enterprise-asset-management/task/repair-req-eam-assets-using-catalog.md).

    -   The Inventory view of the Enterprise Asset Workspace

For more information on this request option, see [Create repair orders for enterprise assets in the Inventory view](../../enterprise-asset-management/task/repair-orders-for-eam-assets-in-inventory-view.md).

    -   The Repair option on the corresponding asset record

For more information on this request option, see [Request repair of an enterprise asset using the Repair option](../../enterprise-asset-management/task/repair-requests-using-asset-form-eam.md).

2.  A repair order and corresponding repair order line are created.
3.  A troubleshooting-based repair asset task is automatically generated for the repair order line.

</td></tr><tr><td>

Repair asset task assignment

</td><td>

1.  The repair asset task must be assigned to a user with the sn\_eam.asset\_technician role.
    -   If the task is not already assigned to a user, a new user assignment must be added.
    -   If the task is already assigned to a user, the user assignment can be updated.
2.  After the user assignment is added or updated, the help repair enterprise assets agentic workflow invokes automatically.

**Note:** If the trigger to invoke the workflow is deactivated, the workflow must be invoked manually.

**Note:** The progress of the workflow is always updated and displayed in the Now Assist panel. Users can access the Now Assist panel by selecting the Now Assist icon ![](../../../common/image/icon-ai-sparkle.png) on the page header of their ServiceNow instance.


</td></tr><tr><td>

Repair asset task validation

</td><td>

The asset next best action AI agent validates the repair asset task.**Note:** For the complete list of validation criteria, refer to [Validating repair asset tasks](now-assist-eam-help-repair-enterprise-assets-workflow.md#section_ex2_2pf_rhc).

-   If the validation is successful, the workflow can proceed with helping the user troubleshoot the asset.
-   If the validation is unsuccessful, the task must be updated and then re-validated.

</td></tr><tr><td>

Asset troubleshooting

</td><td>

After the repair asset task is successfully validated, the workflow helps the user troubleshoot the asset.1.  The asset next best action AI agent triggers the evaluate asset AI agent.
2.  The evaluate asset AI agent performs a web search to identify potential asset issues and to generate corresponding troubleshooting steps.

**Note:** All troubleshooting steps are displayed in the Now Assist panel.

3.  The user who is assigned to the repair asset task must perform all troubleshooting steps to determine the asset issue.
4.  In the Now Assist panel, the AI agent asks the user to confirm if the troubleshooting steps helped with determining the asset issue.
5.  Depending on if the troubleshooting steps helped the user, the workflow proceeds as follows:
    -   If the troubleshooting steps helped, the AI agent asks the user to confirm whether the asset is repairable, unrepairable, or redeployable. The workflow then proceeds to [step 6](now-assist-eam-help-repair-enterprise-assets-workflow.md#user-input).

**Note:** If the user confirms that the asset is repairable, a corresponding repair-based repair asset task is automatically generated. The user is automatically assigned to this task.

    -   If the troubleshooting steps did not help, the AI agent refines its web search. The workflow then returns to [step 2](now-assist-eam-help-repair-enterprise-assets-workflow.md#web-search).
6.  The AI agent requests details about the asset issue.
7.  After the user provides all necessary details, the repair asset task is closed.

**Note:** You can view details about the completed troubleshooting steps in the work notes of the repair asset task.

8.  Depending on whether the asset is repairable, unrepairable, or redeployable, the workflow proceeds as follows:
    -   If the asset is repairable, the workflow proceeds with [helping the user repair it](now-assist-eam-help-repair-enterprise-assets-workflow.md#repair).
    -   If the asset is unrepairable, the user must dispose of it. For more information on asset disposals, see [Create a disposal order in the Enterprise Asset Workspace](../../enterprise-asset-management/task/create-eamdisposal-order.md).
    -   If the asset is redeployable, the user can help redeploy it.

</td></tr><tr><td>

Repair asset task validation

</td><td id="repair">

If the user confirmed that the asset is repairable, the asset next best action AI agent validates the corresponding repair-based repair asset task that was automatically generated.**Note:** For the complete list of validation criteria, refer to [Validating repair asset tasks](now-assist-eam-help-repair-enterprise-assets-workflow.md#section_ex2_2pf_rhc).

-   If the validation is successful, the workflow can proceed with helping the user repair the asset.
-   If the validation is unsuccessful, the task must be updated and then re-validated.

</td></tr><tr><td>

Asset repair

</td><td>

After the repair asset task is successfully validated, the workflow helps the user repair the asset.1.  The asset next best action AI agent triggers the repair asset AI agent.
2.  The repair asset AI Agent performs a web search to generate repair steps based on the asset issue that was determined during troubleshooting.

**Note:** All repair steps are displayed in the Now Assist panel.

3.  The user who is assigned to the repair asset task must perform the repair steps.
4.  In the Now Assist panel, the AI agent asks the user to confirm if the repair steps helped with resolving the asset issue.
5.  Depending on if the repair steps helped the user, the workflow proceeds as follows:
    -   If the repair steps helped, the AI agent asks the user to confirm whether the asset was repaired, unrepairable, or redeployable. The workflow then proceeds to [step 6](now-assist-eam-help-repair-enterprise-assets-workflow.md#close-repair-task).
    -   If the repair steps did not help, the AI agent refines its web search. The workflow then returns to [step 2](now-assist-eam-help-repair-enterprise-assets-workflow.md#web-search-repair).
6.  The repair asset task is closed.

**Note:** You can view details about the completed repair steps in the work notes of the repair asset task.

    -   If the repair asset task is closed with a resolution of Repaired, a corresponding Evaluate asset task is automatically generated. The user must then evaluate the repair to confirm if the asset is redeployable or must be disposed of. For more information on evaluating an asset repair, see [Evaluate the repaired asset in the Enterprise Asset Workspace](../../enterprise-asset-management/task/evaluate-repaired-eam-asset-ws.md).
    -   If the repair asset task is closed with a resolution of Unrepairable, the user must dispose of the asset. For more information on asset disposals, see [Create a disposal order in the Enterprise Asset Workspace](../../enterprise-asset-management/task/create-eamdisposal-order.md).
    -   If the repair asset task is closed with a resolution of Redeployable, the user can help redeploy it.

</td></tr></tbody>
</table>## AI agents used in the help repair enterprise assets agentic workflow

The help repair enterprise assets agentic workflow uses the following AI agents to execute tasks that help you manage and complete your enterprise asset repairs and troubleshooting.

<table id="table_ppz_wby_qhc"><thead><tr><th>

AI agent

</th><th>

AI agent role

</th></tr></thead><tbody><tr><td>

Asset next best action AI agent

</td><td>

-   Validates repair asset tasks.
-   Based on the task type of a given repair asset task, the asset next best action AI agent can trigger one of the following AI agents to help manage and complete the task:
    -   Evaluate asset AI agent to manage a troubleshooting-based repair asset task
    -   Repair asset AI agent to manage a repair-based repair asset task

</td></tr><tr><td>

Evaluate asset AI agent

</td><td>

-   Identifies potential asset issues.
-   Generates comprehensive instructions to help troubleshoot assets.
-   Updates and closes troubleshooting-based repair asset tasks.

</td></tr><tr><td>

Repair asset AI agent

</td><td>

-   Generates comprehensive instructions to help repair assets.
-   Updates and closes repair-based repair asset tasks.

</td></tr></tbody>
</table>**Parent Topic:**[Fulfilling repair orders in the Enterprise Asset Workspace](../../enterprise-asset-management/concept/fulfilling-repair-orders-eam.md)

