---
title: Request inventory
description: Request inventory when your stock gets low or you need a part for a particular work order.Create a part requirement to receive parts when you find defective parts in your stockroom or your stock has run out.Request and source multiple parts simultaneously from a single or multiple stockrooms regardless of whether you have a work order task.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Inventory on Mobile Agent, Complete work orders on Mobile Agent, Using Field Service Management, Field Service Management]
---

# Request inventory

Request inventory when your stock gets low or you need a part for a particular work order.

You can request parts from a peer's stockroom or warehouse. If you request parts from your peer agents, a mobile notification is sent to the peer agent from whom you requested the parts. Your peer agent can either accept or reject your request based on the part availability in their stockroom. If you request parts from warehouse, the transfer orders are automatically generated.

You can request inventory in two ways:

-   **Create part requirement**: Select and request a single part with or without the context of work order task.
-   **Create part request**: Select and request multiple parts from a single or multiple stockrooms directly or based out of existing part requirements.

**Parent Topic:**[Inventory on Mobile Agent](easily-track-parts.md)

**Related topics**  


[Track inventory](../task/view-available-parts-inventory.md)

[Accept or reject part requests from peer agents](../task/accept-reject-part-request-mobile.md)

[View transfer order lines for requested parts](../task/source-part-mobile.md)

## Request a single part

Create a part requirement to receive parts when you find defective parts in your stockroom or your stock has run out.

### Before you begin

Role required: wm\_agent

### About this task

You can create a part requirement with or without the context of a work order task.

### Procedure

1.  Open the Now Mobile Agent application.

2.  Request and source parts.

<table id="choicetable_z2w_ytf_ytb"><thead><tr><th align="left" id="d62415e160">

From

</th><th align="left" id="d62415e163">

Do this

</th></tr></thead><tbody><tr><td id="d62415e169">

**My Work**

</td><td>

1.  Tap **My Work**.
2.  In the **My Tasks** section, tap **See All**.
3.  Select the work order task that needs parts.
4.  Tap on the **Parts** tab.
5.  Under part requirements, tap see all
6.  Tap the More actions \(![More actions icon](../image/OverflowIcon.png)\) icon and then select **Create Part Requirement**.


</td></tr><tr><td id="d62415e221">

**Inventory**

</td><td>

1.  Tap **Inventory**.
2.  Tap **My part requirements**.
3.  Tap **Create Part Requirement**.


</td></tr></tbody>
</table>3.  Tap **Model**.

4.  Select a part model.

5.  To associate the part requirement with the **Work order task**, select a work order task.

6.  To view substitutes of the selected part model, select **Search for substitutes**.

7.  In the **Required quantity** field, enter the total quantity of the parts required to complete the task.

8.  In the **Required by date** field, enter the date by which all parts should be delivered.

9.  Enable the **Mandatory** option to specify the parts required to perform the work order task.

10. Tap **Submit**.

    A message appears as the part requirement is created

11. Navigate back to the part requirements list screen and tap the part requirement card.

12. Tap **Find part** to locate the specific part.

    **Note:** If the part is unavailable in your personal stockroom, you are promptly directed to step 14.

13. Source the part that is already available in your stockroom.

    -   To reserve the part for later use, tap **Reserve this part**.
    -   To source the part from a different stockroom, tap **Source it again** and follow the steps 14 through 19.
14. To view substitutes of the selected part model, select **Search for substitutes**.

15. In the **Radius** field, enter the radius in miles to search the parts within the specified distance.

    The system uses your current location as source location and searches for parts within the specified radius.

16. Tap the **Next** icon.

    The stockroom locations appear in an interactive map and as cards in the **Asset map** screen.

    **Note:** The part information card contains the last known location of your peer agents when the following options are enabled in your peer agent's profile and mobile.

    -   The **Geolocation tracked** option in your peer agent's profile controls whether you can see the parts details and their last known location in the information cards.
    -   The **Location Tracking** option in your peer agent's mobile device and Now Mobile Agent app.
17. Tap the stockroom from which you want to receive the parts and then tap **Source part**.

18. Select the stockroom to which the sourced parts will be transferred.

    For example, if you need to receive parts to your stockroom then select your personal stockroom.

19. In the **Quantity** field, enter the quantity of the parts required to complete the task.

20. Tap the **Next** icon.

21. Navigate back to the **Inventory** screen.


### Result

-   If you have requested parts for a specific work order task, the Part Requirements and Transfer Orders related lists are updated automatically in the work order task form.
-   The transfer order lines are generated when you request parts from a warehouse.
-   If the Field Service Advanced Parts Sourcing \[com.snc.fsm\_advanced\_parts\_sourcing\] plugin is activated and **Create part requests for part requirement sourcing** and **Use part request approvals** properties are enabled, you can view the following records.
    -   A part request is created for the specified part requirement with the state as **In progress** and the part request line with the state as **Requested**. To view the status of your requests, navigate to **Inventory** &gt; **My requests**.
    -   A temporary part request \(RITM\) record is created for the requested parts and sent to your agents as a mobile notification. If the property is disabled or you have requested parts from warehouse, the transfer orders are generated automatically in the Draft state.

## Request multiple parts

Request and source multiple parts simultaneously from a single or multiple stockrooms regardless of whether you have a work order task.

### Before you begin

The Field Service Advanced Parts Sourcing \[com.snc.fsm\_advanced\_parts\_sourcing\] plugin must be activated. For more information on the steps to activate a plugin, see [Activate Field Service Management](../../planning-and-policy/task/t_ActivateFieldServiceManagement.md).

Role required: wm\_agent

### About this task

You can create part requests from **My work** and **Inventory** screens with the required quantity, either directly or by fetching them from an existing part requirement.

**Note:**

-   The parts are searched for in the stockrooms based on the defined values in the Part Search Criteria property. For more information, see [Advanced Part Sourcing components](../reference/advanced-part-souring-components.md).
-   Your current location is considered as the source location and searches for stockrooms in the radius as mentioned in the **Maximum part search radius** and **Distance Unit** of your profile.

### Procedure

1.  Open the Now Mobile Agent application.

2.  Request parts with or without a work order task, or from your own requests or parts requirements lists.

<table id="choicetable_z2w_ytf_ytb"><thead><tr><th align="left" id="d62415e631">

To request parts from

</th><th align="left" id="d62415e634">

Do this

</th></tr></thead><tbody><tr><td id="d62415e640">

**Work order task**

</td><td>

1.  In the **My Tasks** section, tap **See All**.
2.  Select the work order task, which must be in the **Accepted** state.
3.  Tap on the **Parts** tab.
4.  Tap **Create part request**.


</td></tr><tr><td id="d62415e679">

**Work order task with existing part requirements**

</td><td>

1.  Tap **My Work**.
2.  Open the work order task that is either in **Accepted** or **Work in progress** state.
3.  Tap on the **Parts** related list.
4.  In the **Part requirements** section, tap **See All**.
5.  Tap **Request parts**.
 **Note:** The **Request parts** option appears only when you have pending part requirements. Note that you can request parts without selecting a part requirement.

</td></tr><tr><td id="d62415e733">

**Missing work order task**

</td><td>

1.  Tap **Inventory**.
2.  Tap **Create part request**.


</td></tr><tr><td id="d62415e757">

**My requests**

</td><td>

1.  Tap **Inventory**.
2.  Tap **My requests** and then **Create part request**.


</td></tr><tr><td id="d62415e785">

**My part requirements**

</td><td>

1.  Tap **Inventory**.
2.  Tap **My part requirements**.
3.  Tap **Request parts**.
 **Note:** **Request parts** option appears only when you have pending part requirements. Note that you can request parts without selecting a part requirement.

</td></tr></tbody>
</table>3.  Select the stockroom to which the requested parts will be received.

    For example, if you need the parts to complete your work order task then select your personal stockroom.

4.  Select **Submit**.

    The part request is created in the Draft state.

5.  Tap **Add parts**.

6.  Add parts to the part request either directly or from a part requirement.

<table id="choicetable_wrg_txw_stb"><thead><tr><th align="left" id="d62415e860">

To

</th><th align="left" id="d62415e863">

Do this

</th></tr></thead><tbody><tr><td id="d62415e869">

**Add parts directly**

</td><td>

1.  Tap **Add parts directly**.
2.  Select a part model.
3.  \(Optional\) Select the work order task for which you need parts to complete the task.
4.  In the **Quantity** field, enter the total quantity of the parts required to complete the task.
5.  In the **Required by date** field, enter the date by which all parts should be delivered.
6.  \(Optional\) View available substitutes of the selected part model by selecting **Include substitute**.
 **Note:** To add multiple parts, repeat these steps.

</td></tr><tr><td id="d62415e915">

**Add from part requirements**

</td><td>

1.  Tap **Add from part requirements**.
2.  Select the part requirement.

**Note:** Select at least one part requirement.

</td></tr></tbody>
</table>7.  Select **Submit**.

    The part request lines are created with the required parts.

8.  Navigate to the part request list screen by tapping the Back icon.

    **Note:** Managers can directly select the stockroom and fetch the parts on behalf of their agents.

9.  Find parts from the available stockrooms.

    -   To locate a specific part, tap **Find part**.
    -   To locate all parts, tap **Find all**.
    **Note:** If the part is available in your personal stockroom, you can reserve the part using the **Reserve this part** option.

    The stockroom locations that have the parts appear in the interactive map and stockroom information cards in the **Stockroom map** screen.

10. Select the stockrooms from which you want to receive the parts.

11. Tap **Confirm stockroom**.

    A success message appears to validate that the parts have been requested from the selected stockroom.


### Result

-   The part request state changes to In progress and the part request line changes to Requested. To view the status of your requests, navigate to **Inventory** &gt; **My requests**.
-   The part requests are sent to the peer agents from whom you have requested parts if the **Use part request approvals** property is enabled. For more information, see [Advanced Part Sourcing components](../reference/advanced-part-souring-components.md).
-   A temporary part request \(RITM\) record is created for the requested parts and sent to your agents as a mobile notification. If the property is disabled or you have requested parts from warehouse, the transfer orders are generated automatically in the Draft state.
-   If you have requested parts for a specific work order task, the Part Requests and Transfer Orders related lists are updated in the work order task form.

