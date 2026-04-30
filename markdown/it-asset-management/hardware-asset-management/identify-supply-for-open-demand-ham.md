---
title: Identify the supply for open demands in the Hardware Asset Workspace
description: Use the Open demands report to determine available stock within local stockrooms and distribution channels to fulfill sourcing requests that are open.
locale: en-US
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage stockrooms with inventory reports in the Hardware Asset Workspace, Manage stockrooms, Use, Hardware Asset Management, IT Asset Management]
---

# Identify the supply for open demands in the Hardware Asset Workspace

Use the Open demands report to determine available stock within local stockrooms and distribution channels to fulfill sourcing requests that are open.

## Before you begin

Role required: asset

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Procurement**.

2.  In the Procurement overview, select **Open demands**.

    The report displays the list of open demands with the following details:

    -   Requests and requested items.
    -   The quantity of the requested model available in local stockrooms that serve the asset location.
    -   The quantity of the requested model available in distribution channel stockrooms that serve the asset location.
    -   The purchase lead time, which is the average time in days it has taken from ordering to receiving assets through new purchase orders.
3.  To view the current stock availability in the local stockrooms for all open requests for a model and determine if there is sufficient quantity, select the number shown in the **Local stockroom quantity** column.

    The available asset quantity is determined by the current state. If two requests from a service location, which is serviced by two or more stockrooms, are for the same model and the available quantity is 100, the report will show 100 available in the local stockroom for both requests. Once one request is fulfilled, the quantity will update to reflect the remaining amount for the other request.

4.  To view the current stock availability in the distribution channel stockrooms for all open requests for a model and determine if there is sufficient quantity, select the number shown in the **Remote stockroom quantity** column.


**Parent Topic:**[Manage stockrooms with inventory reports in the Hardware Asset Workspace](../concept/manage-stockroom-inventory-report-ham.md)

