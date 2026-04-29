---
title: Now Assist for Software Asset Management \(SAM\) AI agent collection to help manage software asset request agentic workflow
description: Use the Help manage software request agentic workflow to fulfill a software request by either allocating the available entitlements or generating a purchase order for the software model.
locale: en-US
release: australia
product: Now Assist for Software Asset Management \(SAM\)
classification: now-assist-for-software-asset-management-sam
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Use agentic workflows, Now Assist for Software Asset Management \(SAM\), Software Asset Management, IT Asset Management]
---

# Now Assist for Software Asset Management \(SAM\) AI agent collection to help manage software asset request agentic workflow

Use the Help manage software request agentic workflow to fulfill a software request by either allocating the available entitlements or generating a purchase order for the software model.

## Help manage software request overview

Use the Help manage software request agentic workflow to automate software asset sourcing through auto allocation or purchase order creation. The Help manage software request AI agents enable faster request resolution, improved operational efficiency, and boost user satisfaction.

The following three scenarios are supported for software requests:

-   User based allocations: a user requests a software model with user-based entitlements.
-   Device based allocations: a user requests a software model with device-based entitlements.

    When a user who has requested the software has multiple devices assigned to them, the agent will ask the fulfiller to select one of the user's devices for the allocation process. If the device is not assigned to the requested item number user during the software fulfillment, then a message appears in the Now Assist panel chat stating that the user has no devices associated. The user needs to associate a device and try again. If the device is assigned after this, then the fulfiller user should initiate a new Now Assist panel chat and provide an utterance in Now Assist panel to fulfill the requested item number, rather than using the existing Now Assist panel chat.

-   Purchase order flow: if no entitlements are available, a purchase order is created.

The Help manage software request agentic workflow needs the following conditions to execute. Once these conditions are met, the agentic workflow is automatically triggered.

-   The requested item is approved.
-   The requested item belongs to a software category.
-   The requested item is not sourced.
-   The **Assigned to** field in the Requested item \[sc-req item\] table is not empty.

The Help manage software request agentic workflow supports both Azure OpenAI Service and Now LLM Service.

## Help manage software request agentic workflow

By automating the sourcing of software assets through auto-allocation or purchase order creation, the agentic workflow speeds up request resolution and boost operational efficiency.

To automatically trigger the Help manage software request workflow for sourcing software requests, follow these steps:

1.  Initiate and approve a software asset request:
    1.  A user with any role creates a software asset request in the Service Catalog application.
    2.  If the requested items in the cart amount to a thousand dollars, the request is automatically approved. For amounts more than a thousand dollars, the request needs to be approved. Auto approval rules can differ from organization to organization; the default amount for auto approval is a thousand dollars.
2.  Assign the software asset request for sourcing:

    1.  Once the request is approved, the procurement\_user role, navigates to the Procurement module that resides in the Asset Workspace. If the Hardware Asset Management application is installed in the Asset Workspace, the name of the workspace changes to Hardware Asset Workspace.
    2.  The procurement\_user role selects the Items tab in the Procurement module and selects a value in the **Assigned to** field for the requested item.

        **Note:** The itil, the procurement\_user, and the now\_assist\_panel\_user roles have access to the Now Assist panel. The fulfiller needs the itil and procurement\_user roles if you have the Now Assist for IT Service Management \(ITSM\) store application installed. If you have the Now Assist for Software Asset Management \(SAM\) store application but not the Now Assist for IT Service Management \(ITSM\) store application, then the fulfiller requires the itil, procurement\_user, and now\_assist\_panel\_user roles to fulfill the request via the Now Assist panel trigger.

    The procurement\_user role gets notified in the Now Assist panel that the software request is getting fulfilled.

    Once the software asset request is assigned, the Help manage software request agentic workflow gets triggered to source the request.

    -   If entitlements are available for the software request, allocations are automatically made.
    -   If entitlements aren’t available, a purchase order is generated. The AI agents take inputs and confirmation from you when needed.
3.  Assign Microsoft 365 licenses based on availability:

    If the requested item is identified as a Microsoft 365 subscription software, the Microsoft license assignment AI agent gets triggered. The AI agent checks for license availability, assigns available licenses to users, and creates a reservation order if there are no available licenses.

    The AI agent veriﬁes if there are available licenses for the requested item on the Microsoft 365 Admin Center.

    1.  If the licenses are available, the AI agent then checks whether group licenses are available for the requested item.
        -   If licenses assigned to Microsoft Entra ID groups are available, then the AI agent checks for single or multiple groups.
            -   If there are multiple groups, the AI agent prompts the user to select a Microsoft Entra ID group. The user gets assigned to the selected group and the license gets assigned to the user.
            -   If there's a single group, the AI agent assigns the user to that group, and the license gets assigned to the user.
        -   If licenses assigned to Microsoft Entra ID groups aren’t available, the AI agent proceeds to check for individual license availability. If individual licenses are available, the AI agent assigns the user to the license in the Microsoft 365 Admin Center. The license assignment is verified at the next user subscription data pull through the Microsoft 365 integration.
    2.  If the licenses aren't available, the AI agent checks for available entitlements.
        -   If the entitlement is available, the AI agent creates a reservation order using the existing entitlement and generates a catalog task to replicate that reservation within the Microsoft 365 Admin Center.
        -   If the entitlement isn’t available, the AI agent generates a catalog task to create entitlement in ServiceNow.

To view the agentic workflow process, navigate to the Asset Workspace or the Hardware Asset Workspace and select the sparkle icon ![sparkle icon for Now Assist](../../../reuse/icons/brand-icons/bus-ai-sparkle.svg) on the top right side of the workspace.

## AI agents used in the Help manage software asset requests agentic workflow

The Help manage software request agentic workflow uses the following AI agents to execute instructions.

<table id="table_fgx_l24_52c"><thead><tr><th>

AI agent

</th><th>

AI agent role

</th></tr></thead><tbody><tr><td>

Software entitlement allocation AI agent

</td><td>

Validates software license requests and allocates licenses from existing inventory when available, using the request item number \(RITM\).

</td></tr><tr><td>

Purchase order creation AI agent

</td><td>

Sources a request item by creating a purchase order. Asks for inputs sequentially and takes user input in case there are multiple options such as with stockrooms, vendors, metric group, or license metrics.

</td></tr><tr><td>

Microsoft license assignment AI agent

</td><td>

Assigns a Microsoft 365 license from the existing inventory when available, using the RITM.The AI agent checks for both group and individual licenses. If the licenses aren't available, the AI agent creates a reservation order.

</td></tr></tbody>
</table>**Parent Topic:**[Using agentic workflows in Now Assist for SAM](using-now-assist-sam-ai-agents-usecases.md)

