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

Integrating the Software Asset Management and Contract Management Pro applications provides access to the following post-signature contract data and workflows within the Software Asset Workspace:

-   **Obligation Management:** Use the Contract Management Pro application's Obligation Management feature within the Software Asset Workspace. If you have the required roles assigned, you can create an obligation record. This record defines specific instructions and obligation tasks required to fulfill the contract obligation. For more information about the Contract Management Pro application's Obligation Management feature, see [Obligation Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-obligation-management.md). For more information about creating and managing obligation tasks in the Software Asset Workspace, see [Manage obligation tasks in the Software Asset Workspace](manage-obligation-tasks-software-asset-workspace.md).
-   **Renewal Management:** Receive proactive notifications and actionable insights regarding upcoming contract renewals.
-   **Metadata and obligation extraction:** Streamline contract management by extracting the key contract metadata and obligations from an uploaded signed contract document using the manage contract repository agentic workflow. You must install the Now Assist in Contract Management \(sn\_cm\_gen\_ai\) plugin. You must also activate the generative AI skills to use the manage contract repository agentic workflow. For more information about installing the plugin and enabling the skills, see [Configure the manage contract repository agentic workflow for Software Asset Management](../../now-assist-sam/task/configure-manage-contract-repository-agentic-workflow.md). For more information about extracting the key contract metadata and obligations from assigned contract, see [Use manage contract repository agentic workflow in the Software Asset Workspace](../../now-assist-sam/concept/manage-contract-repository-workflow.md).

## Roles required for Software Asset Management and Contract Management Pro better together feature

With the Software Asset Management integration for Obligation Management \(sn\_cm\_obligation\) plugin, the required roles are available. The Software Asset Management admin has to assign the roles to the required users.

|Role|Description|
|----|-----------|
|sn\_cm\_obligation.obligation\_admin|Provides administrative access to Obligation management and underlying data.|
|sn\_cm\_obligation.obligation\_fulfiller|Creates obligations and approves, rejects, or cancels obligation tasks within the Software Asset Workspace.|
|sn\_cm\_obligation.obligation\_user|Acts on the assigned obligation task and submits the task within Software Asset Workspace.|
|sn\_cm\_gen\_ai.ai\_contract\_fulfiller|Extracts the information from a signed contract to add it to the software contract.|
|sn\_cm\_gen\_ai.ai\_contract\_config|Activates or deactivates the Contract obligation extraction and Contract metadata extraction skills.|
|now\_assist\_panel\_user|Accesses the Now Assist panel to activate or deactivate the skills.|
|sn\_cm\_gen\_ai.ai\_contract\_admin|Provides administrative access to the manage contract repository agentic workflow. Installs Now Assist in Contract Management Pro \(sn\_cm\_gen\_ai\) plugin and activates the required skills.|

## Plugins required for the Software Asset Management and Contract Management Pro better together feature

The following plugins are required to use the Software Asset Management and Contract Management Pro better together feature:

-   Obligation Management \(sn\_cm\_obligation\)
-   Now Assist in Contract Management Pro \(sn\_cm\_gen\_ai\)

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

**Related topics**  


[Manage obligation tasks in the Software Asset Workspace](manage-obligation-tasks-software-asset-workspace.md)

[Configure the manage contract repository agentic workflow for Software Asset Management](../../now-assist-sam/task/configure-manage-contract-repository-agentic-workflow.md)

[Use manage contract repository agentic workflow in the Software Asset Workspace](../../now-assist-sam/concept/manage-contract-repository-workflow.md)

