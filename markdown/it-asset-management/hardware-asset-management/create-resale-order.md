---
title: Resale hardware assets
description: Enhance asset management by reselling eligible retired hardware assets instead of disposing of them.
locale: en-US
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-11-24"
reading_time_minutes: 2
keywords: [hardware asset resale, resell retired assets]
breadcrumb: [Create a disposal order, Use, Hardware Asset Management, IT Asset Management]
---

# Resale hardware assets

Enhance asset management by reselling eligible retired hardware assets instead of disposing of them.

## Before you begin

Role required: asset

## About this task

**Important:** The asset resale feature is available with Hardware Asset Management version 15.0.0 onwards.

Asset resale is an extension of the asset disposal workflow that enables you to resell eligible retired assets instead of disposing of them. This approach helps reduce waste and save costs, because you can receive credit for assets that you successfully resell. When the Disposal order is in the Documentation stage, you can choose between disposing of or reselling the assets.

## Procedure

1.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Inventory**.

2.  Select the **Disposal orders** tab.

3.  Select the **Number** link to open the disposal order record that is in the Documentation stage.

    The Disposal order form is displayed.

4.  Select the **Hardware Disposal Tasks** tab.

5.  Select the **Number** link to open the Disposal Documentation task.

    The Disposal Documentation form is displayed.

6.  Select the **Planned Assets** tab.

    The list of assets planned for disposal or resell is displayed.

7.  Select the planned asset records that you want to resell.

    The **Sell**, **Dispose**, and **Cancel** buttons are activated.

8.  Select the **Sell** button.

    The Add resale value window is displayed.

9.  In the Add resale value window, do the following:

    1.  Add the resale value for each asset in the Resold value column.

    2.  From the Currency drop-down, select the currency value.

10. Confirm or cancel the resell.

    -   To mark your confirmation and proceed with asset resell, select **Confirm**.
    -   To close the Add resale value window, select **Cancel**.
    On the Planned Assets list, the State, Substate and Resold value column value is updated for the resold assets.

11. Select the **Details** tab and do the following:

    1.  Select the Attach File icon to attach disposal documentation for the planned assets.

    2.  In the Certificate of disposal list, select **Yes**.

        **Note:** You must attach disposal documentation and set the **Certificate of disposal** field to **Yes** to mark the Disposal Documentation task as Completed.

        The Disposal Documentation task is marked as **Closed Complete**.


## Result

When an asset is sold, on the Asset form, the **State** field value is updated to **Retired**, and the **Substate** field value is updated to **Sold**.

## What to do next

When an asset is sold, an expense line is generated for each resold asset. The Amount column value shows the resold value and it’s a negative value. To view the expense line created for the resold asset, do the following:

1.  On the Disposal Documentation task form, select the **Planned Assets** tab.
2.  Select the **Asset display name** link.
3.  Select the **Expense Lines** tab.

**Parent Topic:**[Create a disposal order](create-disposal-order.md)

**Related topics**  


[Create a disposal order](create-disposal-order.md)

[Perform bulk update of resale value for the assets](bulk-update-resale-value-asset-state.md)

