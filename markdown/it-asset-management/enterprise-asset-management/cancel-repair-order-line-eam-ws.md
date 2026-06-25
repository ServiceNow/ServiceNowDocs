---
title: Cancel a repair order line in the Enterprise Asset Workspace
description: Cancel a repair order line that no longer needs to be fulfilled.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/cancel-repair-order-line-eam-ws.html
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Fulfill repair orders manually, Fulfilling repair orders in the Enterprise Asset Workspace, Manage repair of defective assets in your stockroom in the Enterprise Asset Workspace, Create and manage enterprise asset inventory, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Cancel a repair order line in the Enterprise Asset Workspace

Cancel a repair order line that no longer needs to be fulfilled.

## Before you begin

Role required: enterprise\_asset

## Procedure

1.  Navigate to **All** &gt; **Enterprise Asset Workspace** &gt; **Inventory**.

2.  Select the **Repair orders** tab.

3.  Select a repair order that's in the **Draft** or **In progress** stage.

4.  Select the **Repair order lines** tab.

5.  Select the repair order line that you want to cancel.

    You can cancel a repair order line that is not in the Completed stage.

6.  Select **Cancel**.


## Result

-   The stage of the repair order line changes to Cancelled and the state changes to Closed Incomplete.
-   The state of the associated repair asset tasks that were open changes to Closed Incomplete.
-   The stage of the repair order changes to Cancelled only if there aren't any other repair order lines that are in the Troubleshoot, Repair, Evaluate, or Completed stage.

**Parent Topic:**[Manually fulfill repair orders in the Enterprise Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/fulfill-eam-repair-orders-in-ws.md)

**Related topics**  


[View open repair orders for your stockroom in the Enterprise Asset Workspace]()

[Troubleshoot assets requested for repair in the Enterprise Asset Workspace]()

[Complete the repair asset task in the Enterprise Asset Workspace]()

[Evaluate the repaired asset in the Enterprise Asset Workspace]()

[Bulk close asset repair tasks in the Enterprise Asset Workspace]()

[Cancel a repair order in the Enterprise Asset Workspace]()

