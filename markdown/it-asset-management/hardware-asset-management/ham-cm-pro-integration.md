---
title: Hardware Asset Management integration with Contract Management Pro
description: Use the Hardware Asset Management \(HAM\) and Contract Management Pro integration to perform contract and obligation extraction from signed contract documents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/ham-cm-pro-integration.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-08-24"
reading_time_minutes: 3
breadcrumb: [HAM integrations, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Hardware Asset Management integration with Contract Management Pro

Use the Hardware Asset Management \(HAM\) and Contract Management Pro integration to perform contract and obligation extraction from signed contract documents.

**Important:** This feature is available only with Hardware Asset Management Prime SKU, starting from Hardware Asset Management version 16.0.0 and Australia patch 6.

## Types of hardware contract obligations

Hardware contracts carry specific commitments that must be tracked and fulfilled. The following contract types each introduce obligations that require active management:

-   **Leases**

    Lease renewal dates must be monitored to prevent cost increases or unplanned loss of hardware access at expiration.

-   **Maintenance**

    Vendor service levels must be verified against contractual obligations to track performance.

-   **Warranty**

    Warranty coverage must be tracked to avoid unexpected repair costs when coverage lapses.

-   **Purchase**

    Payment terms and minimums must be met to avoid contractual penalties.


## Benefits of integration

Integrating Hardware Asset Management with Contract Management Pro brings contract obligation management directly into the Hardware Asset Workspace, so you can track contractual commitments, manage renewals, and extract obligations from one place. This integration helps to reduce the risk of missed renewal deadlines, vendor service level failures, and compliance penalties. The integration provides access to the following post-signature contract data and workflows within the Hardware Asset Workspace:

-   **Obligation Management**

    Create and manage obligation records and tasks directly from the Hardware Asset Workspace to track and fulfill the responsibilities specified in hardware contracts. For more information, see [Obligation Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-obligation-management.md) in the Contract Management Pro documentation. For more information about creating and managing obligation tasks in the Hardware Asset Workspace, see [Manage obligations in the Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/manage-obligations-in-ham.md).

-   **Renewal Management**

    Receive notifications about contracts that are approaching renewal or expiration dates.

-   **Metadata and obligation extraction**

    Extract key contract metadata and obligations automatically from an uploaded signed contract document using the manage contract repository agentic workflow. You must install Contract Management Pro Prime and ServiceNow Otto for Contract Management Pro \(`sn_cm_gen_ai`\) applications, and activate the generative AI skills to use this workflow. For more information about installing the plugin and enabling the skills, see [Configure the Manage contract repository agentic workflow for HAM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/configure-contract-repo-agentic-workflow-ham.md). For more information about extracting the key contract metadata and obligations from assigned contract, see [Manage contract repository agentic workflow in the Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/manage-contract-repo-agent-flow-ham.md).


## Plugins required for HAM and Contract Management Pro integration

-   Contract Management Pro Prime \(sc\_cm\_pro\)
-   Obligation Management \(sn\_cm\_obligation\)
-   ServiceNow Otto for Contract Management Pro \(sn\_cm\_gen\_ai\)

## Roles required for HAM and Contract Management Pro integration

With the Obligation Management \(sn\_cm\_obligation\) plugin activated, the following roles are available for the HAM administrator to assign.

|Role|Description|
|----|-----------|
|sn\_cm\_obligation.obligation\_admin|Provides administrative access to Obligation Management and underlying data.|
|sn\_cm\_obligation.obligation\_fulfiller|Creates obligations and approves, rejects, or cancels obligation tasks within the Hardware Asset Workspace.|
|sn\_cm\_obligation.obligation\_user|Acts on the assigned obligation task and submits the task within Hardware Asset Workspace.|
|sn\_cm\_gen\_ai.ai\_contract\_fulfiller|Extracts the information from a signed contract to add it to a warranty, maintenance, lease, or purchase contract record.|
|sn\_cm\_gen\_ai.ai\_contract\_config|Activates or deactivates the Contract obligation extraction and Contract metadata extraction skills.|
|now\_assist\_panel\_user|Accesses the ServiceNow Otto panel to activate or deactivate the skills.|
|sn\_cm\_gen\_ai.ai\_contract\_admin|Provides administrative access to the Manage contract repository agentic workflow. Installs ServiceNow Otto for Contract Management Pro \(sn\_cm\_gen\_ai\) plugin and activates the required skills.|

**Parent Topic:**[Hardware Asset Management integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/ham-integrations.md)

**Related topics**  


[Hardware Asset Management integration with Zero Touch Mobility]()

