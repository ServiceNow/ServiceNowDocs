---
title: Procurement overview for Enterprise Asset Workspace
description: View and manage procurement-related details such as procurement requests, purchase orders, sourcing tasks, and receiving slips through the Enterprise Asset Workspace.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Enterprise Asset Workspace, Explore, Enterprise Asset Management, IT Asset Management]
---

# Procurement overview for Enterprise Asset Workspace

View and manage procurement-related details such as procurement requests, purchase orders, sourcing tasks, and receiving slips through the Enterprise Asset Workspace.

The Procurement view in the Enterprise Asset Workspace provides access to actions for managing your open requests, pending purchase orders and transfer orders, and requests that need manager approval.

![Procurement view in the Enterprise Asset Workspace](../image/eam-procurement-view.png "Procurement view")

Select any widget or chart to view more specific details. You can also narrow down your results by using the **Location**, **Stockroom**, and **Domain** filters.

**Note:** The Domain filter is available only when you’ve enabled the Domain Extensions Installer \(com.glide.domain.msp\_extensions.installer\) and Domain Separation \(plugin com.snc.pa.domain\_support\) plugins.

|Widget or chart|Description|
|---------------|-----------|
|Purchase order pending delivery|Count of purchase orders that aren't received and aren't canceled. Only purchase orders that have a status of Requested, Ordered, or Pending Delivery are displayed.|
|Requests pending approval|Count of sourceable and active requests with the request state of Pending approval.|
|Expenditure by vendor|Cost that you've paid to each of your vendors for procuring the inventory. Only purchase orders that have a status of Ordered, Pending Delivery, or Received are listed.|
|Orders by vendor|Counts of purchase orders that have been ordered, are pending delivery, or have been received by individual vendors.|
|Requests by state for last 30 days|Requests created in the last 30 days grouped by their state.|
|Requests that require sourcing|List of requests for which a purchase order, local order, or transfer order hasn't been initiated.|
|Open purchase orders|List of purchase orders that have been requested or ordered or have not been delivered.|

