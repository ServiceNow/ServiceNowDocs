---
title: Use Software Asset Management with Contract Management Pro
description: Leverage advanced contract life cycle capabilities after a contract has been signed using the Obligation Management \(sn\_cm\_obligation\) and the Now Assist in Contract Management Pro \(sn\_cm\_gen\_ai\) plugin.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [software asset management and CM Pro integration, obligation management]
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Use Software Asset Management with Contract Management Pro

Leverage advanced contract life cycle capabilities after a contract has been signed using the Obligation Management \(sn\_cm\_obligation\) and the Now Assist in Contract Management Pro \(sn\_cm\_gen\_ai\) plugin.

The integration of the Software Asset Management and Contract Management Pro applications enable you to access the following post-signature contract data and workflows within the Software Asset Workspace:

-   **Obligation Management:** Use the Contract Management Pro application's Obligation Management feature within the Software Asset Workspace. If you have the required roles assigned, you can create an obligation record to define speciﬁc instructions and obligation tasks required to fulfill the contract obligation. For more information about the Contract Management Pro application's Obligation Management feature, see [Obligation Management](https://www.servicenow.com/docs/access?context=cncore-obligation-management&version=australia&pubname=australia-employee-service-management&ft:locale=en-US). For more information about creating and managing obligation tasks in the Software Asset Workspace, see [Manage obligation tasks in the Software Asset Workspace](manage-obligation-tasks-software-asset-workspace.md).
-   **Renewal Management:** Receive proactive notifications and actionable insights regarding upcoming contract renewals.
-   **Metadata and obligation extraction:** Streamline contract management by extracting the key contract metadata and obligations from an uploaded signed contract document using the manage contract repository agentic workflow. You must install the Now Assist in Contract Management plugin \(sn\_cm\_gen\_ai\) and activate the generative AI skills to use the manage contract repository agentic workflow. For more information about installing the plugin and enabling the skills, see [Configure the manage contract repository agentic workflow for Software Asset Management](../../now-assist-sam/task/configure-manage-contract-repository-agentic-workflow.md). For more information about extracting the key contract metadata and obligations from assigned contract, see [Use manage contract repository agentic workflow in the Software Asset Workspace](../../now-assist-sam/concept/manage-contract-repository-workflow.md).

## Roles required for Software Asset Management and Contract Management Pro better together feature

With the Software Asset Management integration for Obligation Management plugin \(sn\_cm\_obligation\), the required roles are available. The Software Asset Management admin has to assign the roles to the required users.

<table id="table_nfd_21l_zgc"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_cm\_obligation.obligation\_admin

</td><td>

Provides administrative access to Obligation management and underlying data.

</td></tr><tr><td>

sn\_cm\_obligation.obligation\_fulfiller

</td><td>

Obligation fulfiller can create obligations, approve, reject, or cancel obligation tasks within the Software Asset Workspace.

</td></tr><tr><td>

sn\_cm\_obligation.obligation\_user

</td><td>

Obligation user can act on the assigned on an obligation task and submit the task within Software Asset Workspace.

</td></tr><tr><td>

sn\_cm\_gen\_ai.ai\_contract\_fulfiller

</td><td>

Can extract the information from a signed contract to add it to the software contract.

</td></tr><tr><td>

sn\_cm\_gen\_ai.ai\_contract\_config

</td><td>

Can activate or deactivate the Contract obligation extraction and Contract metadata extraction skills.

</td></tr><tr><td>

now\_assist\_panel\_user

</td><td>

Can access the Now Assist panel to activate or deactivate the skills.

</td></tr><tr><td>

sn\_cm\_gen\_ai.ai\_contract\_admin

</td><td>

Provides administrative access to the manage contract repository agentic workflow. Installs Now Assist in Contract Management Pro plugin and activates the required skills.

</td></tr></tbody>
</table>## Plugins required for the Software Asset Management and Contract Management Pro better together feature

The following plugins are required to use the Software Asset Management and Contract Management Pro better together feature:

-   Obligation Management \(sn\_cm\_obligation\)
-   Now Assist in Contract Management Pro \(sn\_cm\_gen\_ai\)

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

**Related topics**  


[Manage obligation tasks in the Software Asset Workspace](manage-obligation-tasks-software-asset-workspace.md)

[Configure the manage contract repository agentic workflow for Software Asset Management](../../now-assist-sam/task/configure-manage-contract-repository-agentic-workflow.md)

[Use manage contract repository agentic workflow in the Software Asset Workspace](../../now-assist-sam/concept/manage-contract-repository-workflow.md)

