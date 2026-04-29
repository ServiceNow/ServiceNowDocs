---
title: View stockroom details
description: View detailed information about the stockrooms where your hardware, consumables, bundles, pallets, loaner, enterprise, and other assets are located.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage stockrooms, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# View stockroom details

View detailed information about the stockrooms where your hardware, consumables, bundles, pallets, loaner, enterprise, and other assets are located.

## Before you begin

Role required: admin or asset

## Procedure

1.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Inventory**.

2.  Select the **All stockrooms** tab.

3.  From the list of available stockrooms, select the stockroom.

4.  View details about the stockroom on the Details tab.

    View the following details about the stockroom:

    -   All open tasks associated with the stockroom through the Open stockroom task cards. Selecting a card displays a list of the task records.
    -   The active stock rules of your stockroom. The stock rule cards from the contextual sidebar help you know if the stock is less than the threshold and if the model has reached the end of sale.
    -   The hours that the stockroom is available are shown in the **Hours of operation** field.
    -   The location of the stockroom based on the specified address is shown in the interactive map. To view all service locations and distribution channels associated with the stockroom, select **Toggle full screen view**.
    -   Options to enable AI agents in the Help manage hardware asset requests agentic workflow to source hardware assets requests autonomously are available in the Sourcing by AI agents section. The auto-sourcing options include the following:

        -   **Auto-consume**
        -   **Auto-transfer**
        -   **Auto-purchase**
        For more details, see [Configure a stockroom for automated sourcing by AI agents](configure-stockroom-auto-sourcing.md) and [Now Assist for Hardware Asset Management \(HAM\) AI agent collection Help manage hardware asset requests agentic workflow](../../now-assist-ham/concept/now-assist-ham-fulfill-req-agent-workflow.md).

5.  On the Task timeline tab, view the timeline of all scheduled stockroom tasks and the inbound shipments, outbound shipments, and work activities associated with those tasks.

6.  On the **Task timeline** tab, adjust the timeline view and timeline duration.

    -   Set the view to the calendar view with a specified time duration by selecting one of the following values from the **Calendar** drop-down list in the top right:
        -   **Day**
        -   **Work week**
        -   **Week**
        -   **Month**
    -   Set the view to the timeline view with a specified time duration by selecting one of the following values from the **Timeline** drop-down list in the top right:
        -   **Day**
        -   **Week**
        -   **4 Weeks**
7.  View the service locations and distribution channels of the stockroom and details of different types of assets in the stockroom by selecting the tabs corresponding to the asset type.

    **Note:** The tabs related to the enterprise assets appear only if the Enterprise Asset Management application is installed on your ServiceNow® instance. If you select an enterprise asset, you’re automatically redirected to the corresponding record in the Enterprise Asset Workspace. If you have access to an enterprise asset, you also have access to the Enterprise Asset Workspace. For more details, see [Enterprise Asset Workspace](../../enterprise-asset-management/concept/using-eam-workspace.md).


**Parent Topic:**[Manage stockrooms](../concept/manage-your-stockrooms.md)

