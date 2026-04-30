---
title: Asset reclamation
description: Reclaim Asset catalog item integrates Asset Management module with HR module to let you efficiently reclaim assets.
locale: en-US
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Explore, Hardware Asset Management, IT Asset Management]
---

# Asset reclamation

Reclaim Asset catalog item integrates Asset Management module with HR module to let you efficiently reclaim assets.

When an employee leaves an organization or moves to a different role, reclaiming the assets assigned to the employee is a troublesome task and needs much coordination between the HR professional and the asset manager. The Reclaim Asset catalog item has prescriptive workflows to efficiently reclaim hardware assets and store them in the inventory, reassign, send it for repair, or dispose of as required.

An HR professional, manager, or employee can submit an asset reclamation request using the Reclaim Asset catalog item. A manager can submit an asset reclamation request for the reporting members. An HR professional can submit an asset reclamation request for any employee in the organization. An employee other than an HR professional and a manager can submit an asset reclamation request for self. For more information, see [Submit an asset reclamation request](../task/submit-asset-reclamation-request.md).

**Note:** You can't reclaim asset bundles and pallets.

When you create a Reclaim Asset request via Service Catalog, an Asset Reclamation Request is created. For each hardware or consumable assigned to the departing employee, a Hardware Asset Reclamation Line is created for the assets you select in the Reclaim Asset Service Catalog. Each Hardware Asset Reclamation Line is closed through the following Hardware Asset Reclamation Tasks:

-   Schedule drop off, Schedule pickup, or Schedule shipment task based on which reclamation method you select in the Reclaim Asset form
-   Receive asset
-   Evaluate

The Hardware Asset Reclamation Line also has a stage field, which changes when you close a Hardware Asset Reclamation Task as follows:

-   Ready
-   Pending receive
-   Pending evaluation
-   Complete

For more information, see [Close an asset reclamation request](../task/close-asset-reclamation-request.md).

The Hardware Asset Reclamation Sub Flow decision table enables you to trigger your custom reclamation sub flow for hardware and consumable assets. Based on the condition related to the asset that you specify in the decision table, the corresponding sub flow is triggered, and the reclamation process completes.

To use Service Catalog Request, you must install SAM Professional or HAM Professional. If you have installed only SAM Professional, you can access the Service Catalog, but only the Software Asset Reclamation flow gets triggered.

