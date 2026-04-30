---
title: Now Assist for Hardware Asset Management \(HAM\) AI agent collection Help manage hardware asset requests agentic workflow
description: Use the Help manage hardware asset requests agentic workflow, driven by AI agents, to handle your employees' hardware asset requests automatically. The AI agents fulfill requests by either consuming the available local stock, or by generating transfer orders or purchase orders.
locale: en-US
release: yokohama
product: Now Assist for Hardware Asset Management
classification: now-assist-for-hardware-asset-management
topic_type: concept
last_updated: "2025-04-02"
reading_time_minutes: 7
keywords: [AI Agents, agentic AI]
breadcrumb: [Use agentic workflows, Now Assist for Hardware Asset Management \(HAM\), Hardware Asset Management, IT Asset Management]
---

# Now Assist for Hardware Asset Management \(HAM\) AI agent collection Help manage hardware asset requests agentic workflow

Use the Help manage hardware asset requests agentic workflow, driven by AI agents, to handle your employees' hardware asset requests automatically. The AI agents fulfill requests by either consuming the available local stock, or by generating transfer orders or purchase orders.

## Help manage hardware asset requests agentic workflow overview

The AI agents in the Help manage hardware asset requests agentic workflow help to speed up request resolution, improve operational efficiency, and enhance user satisfaction. This agentic workflow processes and fulfills requests for hardware, consumables, bundles, and pallets.

**Note:** The itil, the procurement\_user, and the now\_assist\_panel\_user roles have access to the Now Assist panel. The fulfiller needs the itil and procurement\_user roles if you have the Now Assist for IT Service Management \(ITSM\) store application installed. If you have the Now Assist for Hardware Asset Management \(HAM\) store application but not the Now Assist for IT Service Management \(ITSM\) store application, then the fulfiller requires the itil, procurement\_user, and now\_assist\_panel\_user roles to fulfill the request via the Now Assist panel trigger.

-   **Auto-sourcing scenarios**

    To enable AI agents to perform sourcing autonomously, the following options are available at the stockroom level:

    -   **Auto-consume**: Automatically use the available local stock.

        Automatic consumption of local stock happens when a minimum of one stockroom serving the location of the requester has the **Auto-consume** option enabled. If several stockrooms at the location of the requester have the **Auto-consume** option enabled, assets are first consumed from the stockroom with the highest available quantity. If there are still assets needed, they’re consumed from the stockroom with the next highest quantity.

    -   **Auto-transfer**: Automatically transfer stock from another stockroom.

        Automatic transfer of assets happens under the following conditions:

        -   There’s only one destination stockroom serving the location of the requester that has the **Auto-transfer** option enabled.
        -   The destination stockroom must be linked to distribution channels that serve as source stockrooms. Sourcing from these channels is based on their rank, beginning with the distribution channel having the lowest rank and moving on to the next ranks.
        -   The **Auto-transfer** option is enabled on both the source and destination stockrooms.
        .

    -   **Auto-purchase**: Automatically create purchase orders to procure assets from a vendor.

        Automatic purchase of assets happens under the following conditions:

        -   There’s only one stockroom serving the location of the requester that has the **Auto-purchase** option enabled.
        -   There’s only one vendor from whom the model of the requested item can be purchased.
-   **Requested item \(RITM\) validations**

    Before sourcing any hardware asset requests, the Help manage hardware asset requests agentic workflow validates the requested item \(RITM\). The agentic workflow doesn't proceed with sourcing under the following conditions:

    -   The RITM number is missing or invalid.
    -   More than one requested items have the same RITM number.
    -   The requested item is already sourced.
    -   The request isn't sourceable.
    -   The request isn’t approved.
    -   The model that’s requested is invalid or missing.
    -   The model isn’t associated with any model category.
    -   The resource category of the requested model isn’t opted in.
    -   The model associated with the catalog item isn’t licensed.
-   **Stages in the agentic workflow**

    The fulfillment of hardware asset requests through the agentic workflow includes the following stages:

    1.  Hardware asset request initiation
        1.  An employee creates a hardware asset request in the Service Catalog application.
        2.  The request is either automatically approved or, when necessary, approved by the asset manager.
        3.  The requested item is assigned to a procurement user, which triggers the Help manage hardware asset requests agentic workflow.
    2.  Asset availability checks by the AI agent
        1.  The AI agent verifies whether the requested item is available in the inventory.
        2.  The AI agent also checks the stockrooms that are set up for automatic consumption of local stock, transfer, and purchase.
    3.  Asset sourcing and allocation
        1.  When stockrooms are configured to consume, transfer, and purchase assets automatically through the AI agents, the following events occur:
            1.  The AI agent first uses the available stock in the stockroom.
            2.  For any remaining assets that can be transferred from another stockroom, the AI agent creates a transfer order.
            3.  If there are still assets to be sourced, the AI agent creates a purchase order to buy them from a vendor.
        2.  When assets are available in stockrooms that aren't set up for automatic sourcing, the AI agent creates a sourcing plan and asks for confirmation from the assignee of the requested item \(RITM\) or the person who started the conversation through the Now Assist panel before proceeding.

            **Note:** To access the Now Assist panel after it has been activated, you should have the now\_assist\_panel\_user role. To access the Help manage hardware asset requests agentic workflow in the Hardware Asset Workspace, select the sparkle icon.

            ![Conversation in the Now Assist panel](../image/now-assist-ham-ai-workflow.png "Conversations in the Now Assist panel")

            1.  If the AI agent receives the confirmation to proceed and there have been no changes to the plan, it sources the assets according to the sourcing plan.

                **Note:** If there's a change in the plan, the agentic workflow stops, and the conversation should be reinitiated through the Now Assist panel.

            2.  If the AI agent receives a confirmation not to proceed with the sourcing plan, or if there's still some quantity of assets remaining to be sourced, the agentic workflow continues as follows:
                1.  The AI agent first verifies whether the assets can be sourced through a transfer order or purchase order.

                    If the transfer is possible, the following events happen:

                    1.  The AI agent asks to confirm whether it can proceed with the transfer.
                    2.  If the AI agent receives confirmation to proceed, it asks to confirm both the source and destination stockrooms.
                    3.  After receiving confirmation, the AI agent creates a transfer order.
                    **Note:** If there’s only one stockroom available as the source or destination, it’s automatically selected. The AI agent displays only the source stockrooms that have the quantity of assets to be sourced. Only the stockrooms that serve the location of the requester are shown as destination stockrooms.

                2.  If the AI agent receives a confirmation not to proceed with the transfer order:

                    1.  The AI agent further requests confirmation to proceed with the purchase order.
                    2.  If the AI agent receives confirmation to proceed, it asks to confirm the vendor and the destination stockroom.
                    3.  After receiving confirmation, the AI agent creates a purchase order.
                    **Note:** If there's only one stockroom or vendor available, these values are automatically selected. The AI agent displays the list of vendors for the requested item. Only the stockrooms that serve the location of the requester are shown as destination stockrooms.

                3.  If the user doesn't agree to either the transfer order or the purchase order, the request must be sourced manually.

Refer to the information provided here on the AI agents related to the Help manage hardware asset requests agentic workflow.

To modify the Help manage hardware asset request agentic workflow [duplicate it](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US), and adjust the settings according to your requirements.

**Important:** In the Edit trigger form, make sure that the **Active** button is turned on to enable the AI agent to trigger autonomously.

## AI agents used in the Help manage hardware asset requests agentic workflow

The Help manage hardware asset requests agentic workflow uses specific AI agents to consume local stock, transfer assets between stockrooms, and procure assets from vendors.

<table id="table_hyw_1mh_y2c"><thead><tr><th>

AI agent

</th><th>

AI agent role

</th></tr></thead><tbody><tr><td>

Hardware asset management sourcing AI agent

</td><td>

-   The AI agent checks if the requested item is available in the stockroom. Depending on the automatic sourcing set up in the stockroom, the AI agent either uses the local stock autonomously or creates a sourcing plan and requests user confirmation to consume the assets.
-   Triggers the Transfer order creation AI agent to create transfer orders.
-   Triggers the Purchase order creation AI agent to create purchase orders.

</td></tr><tr><td>

Transfer order creation AI agent

</td><td>

Sources the requested item by either creating a transfer order autonomously or according to the sourcing plan created by the Hardware asset management sourcing AI agent. If there are multiple source or destination stockrooms, the AI agent requests user input to create the transfer order.

</td></tr><tr><td>

Purchase order creation AI agent

</td><td>

Sources the requested item by either creating a purchase order autonomously or according to the sourcing plan created by the Hardware asset management sourcing AI agent. If there are multiple destination stockrooms or vendors, the AI agent requests user input to create the purchase order.

</td></tr></tbody>
</table>## Access the Help manage hardware asset requests agentic workflow in the AI Agent Studio

-   Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
-   Select **Help manage hardware asset requests**.

**Parent Topic:**[Using agentic workflows in Now Assist for HAM](now-assist-ham-agentic-workflow.md)

**Related topics**  


[Now Assist for Hardware Asset Management \(HAM\) AI agent collection Help repair hardware assets agentic workflow](now-assist-ham-repair-agent-workflow.md)

