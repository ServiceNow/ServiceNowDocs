---
title: Identify the supply and demand for models within a stockroom in the Enterprise Asset Workspace
description: Use the Supply vs Demand report to evaluate the available and incoming quantity of models in your stockroom and the requests for these models from different service locations. This report helps you determine if you have enough assets to meet the demand.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Manage stockrooms with inventory reports in the Enterprise Asset Workspace, Create and manage enterprise asset inventory, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Identify the supply and demand for models within a stockroom in the Enterprise Asset Workspace

Use the Supply vs Demand report to evaluate the available and incoming quantity of models in your stockroom and the requests for these models from different service locations. This report helps you determine if you have enough assets to meet the demand.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_technician or sn\_eam.enterprise\_asset\_manager

## About this task

Supply refers to the assets that are currently in stock and those that are incoming at your stockroom. Demand refers to the requests for assets from different service locations that your stockroom services.

Note the following points about the Supply vs Demand report:

-   Supply of an asset model to your stockroom includes:
    -   In stock assets that are in the Available, Reserved, Pending transfer, and Pending install substate
    -   Incoming transfer orders that are partially shipped, fully shipped, in transit, received, and delivered
    -   Incoming purchase orders that are ordered
-   Demand for an asset model includes:
    -   Outgoing transfer orders that are in the Draft, Requested, and Shipment preparation stage
    -   Asset requests
    -   Refresh requests
    -   Work order parts requests

The supply and demand details are stored in the Model and stockrooms \[sn\_asset\_model\_and\_stockroom\] table. The **Populate model and stockroom data** scheduled job runs daily to populate this table.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace** &gt; **Inventory**.

2.  Select the **All stockrooms** tab.

3.  From the list of stockrooms, select the one for which you want to view the supply and demand details.

4.  Select the **Inventory insights** tab.

    ![Supply vs Demand report](../image/supply-demand-report-eam.png "Supply vs Demand report")

    The Supply vs Demand report shows the count on the y-axis and the model on the x-axis, with separate bars for supply and demand for each model. This visual representation helps you to compare the available quantity of each model in the stockroom with the number of requests from different service locations. By looking at the graph, you can determine which models have enough supply to meet demand and which ones need more stock.

    **Note:** By default, the graph shows details for only 10 models.

5.  View the details of the model that isn't shown on the report.

    1.  Select the **Model** filter.

    2.  Enter the model in the search field or select the model from the **Available** list.

    3.  Move the selected model to the **Applied** list.

    4.  Select **Apply**.

6.  To further drill down into the supply or demand for a model and view its component-level details, select the corresponding bar.

    -   The supply graph shows the count of the following:
        -   **In stock assets**: Number of associated assets that are currently in the In stock state and Available, Reserved, Pending transfer, and Pending install substate within the given stockroom.
        -   **Incoming transfer order**: Number of associated assets that are currently being transferred to the given stockroom. This number is based on the sum of the **Quantity remaining** field value for all associated transfer order lines.
        -   **Incoming purchase order**: Number of associated assets that have been ordered but not yet delivered to the given stockroom. This number is based on the sum of the **Remaining quantity** field value for all associated purchase order lines.
    -   The demand graph shows the count of the following:
        -   **Outgoing transfer order**: Number of associated assets that are currently being transferred from the given stockroom. This number is based on the sum of the **Quantity requested** field value for all associated transfer order lines.
        -   **Asset requests**: Number of associated enterprise asset requests. This number is based on the sum of the **Quantity** field value for all associated request items.
        -   **Refresh requests**: Number of associated enterprise asset refresh requests. TThis number is based on the sum of the **Quantity** field value for all associated request items.
        -   **Work order parts requests**: Number of parts requests for associated work orders and work order tasks. This number is based on the sum of the **Quantity** field value for all associated request items.
    By selecting the relevant bars, you can view the list of assets that make up the count.

7.  To initiate the calculation of supply and demand for asset models manually, select **Recalculate quantity**.

    The Supply vs Demand graph updates to show the recently calculated values.


**Parent Topic:**[Manage stockrooms with inventory reports in the Enterprise Asset Workspace](../concept/manage-stockroom-inventory-reports.md)

