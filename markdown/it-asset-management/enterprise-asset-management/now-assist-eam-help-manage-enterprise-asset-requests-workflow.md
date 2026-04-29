---
title: Fulfill enterprise asset requests by using the help manage enterprise asset requests agentic workflow
description: You can use the help manage enterprise asset requests agentic workflow to fulfill enterprise asset requests autonomously. The workflow uses a collection of AI agents to automatically source assets for these requests.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Fulfilling enterprise asset requests, Using Service Catalog for Enterprise Asset Management requests and flows, Enterprise Asset Management, IT Asset Management]
---

# Fulfill enterprise asset requests by using the help manage enterprise asset requests agentic workflow

You can use the help manage enterprise asset requests agentic workflow to fulfill enterprise asset requests autonomously. The workflow uses a collection of AI agents to automatically source assets for these requests.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Help manage enterprise asset requests agentic workflow overview

The help manage enterprise asset requests agentic workflow automates the enterprise asset sourcing process so that you can fulfill enterprise asset requests with little to no human intervention. This automation can help provide the following benefits:

-   Increases request resolution.
-   Improves operational efficiency.
-   Enhances and simplifies the user experience.

Based on the available inventory across your stockrooms, the workflow uses AI agents to automatically source assets through one of the following options:

<table id="table_spm_gql_4hc"><thead><tr><th>

Sourcing option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Local inventory

</td><td>

The AI agent automatically uses assets that are available in a local stockroom.

 This sourcing option is available only when at least one stockroom within the location of the requester has the **Auto-consume** option enabled. If multiple stockrooms have this option enabled, the AI agent uses assets from the stockroom with the highest available quantity first. If any additional assets are required, the AI agent then uses assets from the stockroom with the next highest quantity.

 **Note:** For instructions on how to enable the **Auto-consume** option, see [Create stockroom for enterprise assets](../../enterprise-asset-management/task/create-eamstockroom.md).

</td></tr><tr><td>

Transfer order

</td><td>

The AI agent automatically generates a transfer order to move assets between stockrooms.

 This sourcing option is available only under the following conditions:

-   At least one destination stockroom within the location of the requester has the **Auto-transfer** option enabled.
-   At least one source stockroom has the **Auto-transfer** option enabled.
-   Destination stockrooms are linked to source stockrooms through distribution channels. The order of stockrooms that you can source and transfer assets from is based on the rank of each stockroom.

For more information on distribution channels, see [Add a distribution channel to a stockroom in the Enterprise Asset Workspace](../../enterprise-asset-management/task/add-distribution-channel-eam-stockroom.md).


 **Note:** For instructions on how to enable the **Auto-transfer** option, see [Create stockroom for enterprise assets](../../enterprise-asset-management/task/create-eamstockroom.md).

</td></tr><tr><td>

Purchase order

</td><td>

The AI agent automatically generates a purchase order to obtain additional assets.

 This sourcing option is available only under the following conditions:

-   At least one stockroom within the location of the requester has the **Auto-purchase** option enabled.
-   At least one vendor is available to purchase the requested asset from.

 **Note:** For instructions on how to enable the **Auto-purchase** option, see [Create stockroom for enterprise assets](../../enterprise-asset-management/task/create-eamstockroom.md).

</td></tr></tbody>
</table>**Important:** You can enable security implementation to execute AI agents and agentic workflows through Access Control Lists \(ACLs\) and user identities. ACLs provide the Run As capability to let agents and agentic workflows execute actions either as a dynamic user or as an AI user. For more information, see [Implement access control in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

**Important:** By default, all agentic workflows and AI agent records are read-only.

## Role masking

Agentic workflows and their AI agents use [role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Validating enterprise asset requests

Before the help manage enterprise asset requests agentic workflow can begin sourcing assets for an enterprise asset request, it must validate the request. The workflow proceeds only if the request meets the following criteria:

-   The request has been approved.
-   Each requested asset can be sourced.
-   Each requested asset has not already been sourced.
-   Each asset is either requested directly from the Enterprise Catalog or associated with one of the following models:
    -   Any valid enterprise model
    -   Any valid hardware model that is supported by the OT Asset Management application
-   Each requested asset corresponds with a requested item \(RITM\) under the enterprise asset request. Each RITM has a valid and unique RITM number.
-   Each RITM is assigned to a user with the asset\_manager role.

## Stages in the help manage enterprise asset requests agentic workflow

The help manage enterprise asset requests agentic workflow fulfills enterprise asset requests through the following stages:

<table id="table_jrn_dyg_phc"><thead><tr><th>

Stage

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Enterprise asset request initiation

</td><td>

1.  A user with any role submits an enterprise asset request in the Service Catalog application.

**Note:** Each asset that the user requests corresponds with a requested item \(RITM\) under the enterprise asset request.

2.  Depending on the total cost of the requested assets, the request is approved either automatically or by an asset manager.

    -   If the total cost of the requested assets is less than the amount specified in the corresponding automatic approval rule, the request is approved automatically. By default, this amount is set to one thousand dollars.
    -   If the total cost of the requested assets is more than the amount specified in the corresponding automatic approval rule, the request must be reviewed and approved by an asset manager.
For more information on automatic approval rules, see [Set automatic approval rules](https://www.servicenow.com/docs/access?context=r_SetAutomaticApprovalRules&version=australia&pubname=australia-build-workflows&ft:locale=en-US).


</td></tr><tr><td>

Asset sourcing assignment

</td><td>

1.  After the request is approved, each RITM must be assigned to a user with the asset\_manager role.
2.  After each RITM is assigned to a user, the help manage enterprise asset requests agentic workflow invokes automatically.

**Note:** If the trigger to invoke the workflow is deactivated, the workflow must be invoked manually.

**Note:** The progress of the workflow is always updated and displayed in the Now Assist panel. Users can access the Now Assist panel by selecting the Now Assist icon ![](../../../common/image/icon-ai-sparkle.png) on the page header of their ServiceNow instance.


</td></tr><tr><td>

Enterprise asset request validation

</td><td>

The workflow validates the request.**Note:** For the complete list of validation criteria, refer to [Validating enterprise asset requests](now-assist-eam-help-manage-enterprise-asset-requests-workflow.md#section_k3b_sbm_4hc).

-   If the validation is successful, the workflow can proceed with sourcing the requested assets.
-   If the validation is unsuccessful, the request must be updated and then re-validated.

</td></tr><tr><td>

Asset sourcing and allocation

</td><td>

After the request is successfully validated, the workflow sources the requested assets.1.  The asset sourcing AI agent checks if the requested assets are available in any local stockrooms.
    -   If the requested assets are available, the AI agent checks if the **Auto-consume** option is enabled for any stockrooms that those assets are located in.
        -   If the **Auto-consume** option is enabled, the AI agent uses assets from those stockrooms.
        -   If the **Auto-consume** option is disabled, the workflow proceeds to [step 4](now-assist-eam-help-manage-enterprise-asset-requests-workflow.md#user-intervention).
    -   If the requested assets are not available, or if additional assets must still be sourced, the workflow proceeds to [step 2](now-assist-eam-help-manage-enterprise-asset-requests-workflow.md#transfer-order).
2.  The asset sourcing AI agent checks if the requested assets are available in any non-local stockrooms.
    -   If the requested assets are available, the AI agent checks if the **Auto-transfer** option is enabled for any stockrooms that those assets are located in.
        -   If the **Auto-transfer** option is enabled, the AI agent triggers the transfer order creation AI agent. This AI agent creates a transfer order to move the requested assets from a source stockroom to a destination stockroom. If multiple source or destination stockrooms are available, the AI agent requests user input when creating the transfer order.

**Note:** In this scenario, non-local stockrooms act as source stockrooms, while local stockrooms act as destination stockrooms.

        -   If the **Auto-transfer** option is disabled, the workflow proceeds to [step 4](now-assist-eam-help-manage-enterprise-asset-requests-workflow.md#user-intervention).
    -   If the requested assets are not available, or if additional assets must still be sourced, the workflow proceeds to [step 3](now-assist-eam-help-manage-enterprise-asset-requests-workflow.md#purchase-order).
3.  The asset sourcing AI agent checks if the **Auto-purchase** option is enabled for any local stockrooms.
    -   If the **Auto-purchase** option is enabled, the AI agent triggers the purchase order creation AI agent. This AI agent creates a purchase order to obtain assets from a specified vendor. If multiple vendors are available, the AI agent requests user input when creating the purchase order.
    -   If the **Auto-purchase** option is disabled, the workflow proceeds to [step 4](now-assist-eam-help-manage-enterprise-asset-requests-workflow.md#user-intervention).
4.  If the requested assets cannot be sourced automatically, user intervention is required.
    1.  The asset sourcing AI agent creates sourcing plans to confirm how it should proceed with sourcing each requested asset.
    2.  The AI agent launches the Now Assist panel to initiate a conversation with each user who is assigned to a requested asset.
    3.  After reviewing the sourcing plan for an assigned asset, each user must either accept or reject the plan.
    4.  Depending on whether a user accepts or rejects a sourcing plan, the workflow proceeds as follows:
        -   If a user accepts a sourcing plan without requesting any modifications, the relevant AI agent sources the asset accordingly.

**Note:** If any modifications are required at a later time, the user must re-initiate the conversation in the Now Assist panel.

        -   If a user rejects a sourcing plan, the requested asset must be sourced manually.

</td></tr></tbody>
</table>## AI agents used in the help manage enterprise asset requests agentic workflow

The help manage enterprise asset requests agentic workflow uses the following AI agents to execute tasks for fulfilling enterprise asset requests.

<table id="table_rwp_my4_nhc"><thead><tr><th>

AI agent

</th><th>

AI agent role

</th></tr></thead><tbody><tr><td>

Asset sourcing AI agent

</td><td>

Initiates the sourcing process for a requested asset. The AI agent prioritizes sourcing the asset from a local stockroom. If the asset is not available, or if the corresponding asset sourcing option is not enabled, the AI agent can trigger one of the following order creation AI agents to create either a transfer order or purchase order for the asset:-   Transfer order creation AI agent to create a transfer order
-   Purchase order creation AI agent to create a purchase order

</td></tr><tr><td>

Transfer order creation AI agent

</td><td>

Sources the requested asset by creating a transfer order. If you have multiple source or destination stockrooms, the AI agent requests user input when creating the transfer order.

</td></tr><tr><td>

Purchase order creation AI agent

</td><td>

Sources the requested asset by creating a purchase order. If you have multiple destination stockrooms or vendors, the AI agent requests user input when creating the purchase order.

</td></tr></tbody>
</table>**Parent Topic:**[Fulfilling enterprise asset requests](../../enterprise-asset-management/concept/fulfilling-enterprise-asset-requests.md)

