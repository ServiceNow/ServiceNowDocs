---
title: Source requests from Enterprise Asset workspace
description: You can create a request in the Service Catalog application and source that request from the Enterprise Asset Workspace.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Procuring enterprise assets, Enterprise Asset Management, IT Asset Management]
---

# Source requests from Enterprise Asset workspace

You can create a request in the Service Catalog application and source that request from the Enterprise Asset Workspace.

## Before you begin

You can source a request by using assets from the requester's local stockroom, if stock is available in the local stockroom. If stock is unavailable in the local stockroom, you can get the assets transferred from other stockrooms or create a purchase order.

Role required: proc\_user

## Procedure

1.  Navigate to **Enterprise Asset Workspace** &gt; **Procurement** &gt; **Catalog tasks**.

2.  Open the sourcing task for the request and select **Source request**.

3.  On the Sourcing page, select either of these three options:

    -   **Consume**: If the stock is available in your local stockroom.

        If the Asset pick task is enabled for the source stockroom, the task is added to the Enterprise Asset Refresh Request and Enterprise Asset Request flows.

    -   **Transfer**: If the stock isn’t available in your local stockroom and you want to source the request via a transfer order.

        **Note:** If you create a transfer order and want the local stockroom to be included in the list of stockrooms to choose from, the admin must turn on the `glide.asset.procurement.sourcing.local_stock_transfer` property.

    -   **Purchase**: If the stock isn’t available in your local stockroom and you want to source a request via a purchase order.
4.  Fill in the required fields based on the option that you choose.

5.  Select **Submit**.

    A task for transfer order line or purchase order line is created if you selected **Transfer** or **Purchase**. You can open the request to view the task.


**Parent Topic:**[Procuring enterprise assets](../concept/procuring-assets.md)

