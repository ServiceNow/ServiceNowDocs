---
title: Enterprise asset reclamation
description: Use a reclamation workflow to coordinate an employee's offboarding process that lets you request, assess, and reclaim enterprise assets.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Exploring Enterprise Asset Management, Enterprise Asset Management, IT Asset Management]
---

# Enterprise asset reclamation

Use a reclamation workflow to coordinate an employee's offboarding process that lets you request, assess, and reclaim enterprise assets.

When an employee leaves an organization or moves to a different role, retrieving the assets assigned to the employee needs extensive coordination between the Human Resources department and the enterprise asset managers. You can create an offboarding service catalog request, which initiates a prescriptive workflow to efficiently retrieve assets and restock them in the inventory, reassign them, send them for repair, or dispose as required.

You can create an asset reclamation request via the Service Catalog application. After the request is created, reclamation line items are created that comprise a series of tasks. These tasks can only be accessed and performed by the sam\_user role. After all the tasks are closed, the reclamation line item is complete. After all the reclamation line items are complete, the catalog request is also completed.

**Note:** To use the Service Catalog application to reclaim enterprise assets, you must install the Enterprise Asset Management application.

When you [create a reclaim asset](../task/create-enterprise-catalog-request.md) request via the Service Catalog application, an asset reclamation request is created. For each enterprise asset assigned to the departing employee, an enterprise asset reclamation line is created for the assets you select in the Reclaim Asset Service Catalog. Each enterprise asset reclamation line is closed through the following Enterprise Asset Reclamation Tasks:

-   Schedule drop off, Schedule pickup, or Schedule shipment task based on which reclamation method you select in the Reclaim Asset form
-   Receive asset
-   Evaluate

The Enterprise Asset Reclamation Line also has a stage field, which changes when you [close a Enterprise Asset Reclamation Task](../task/close-enteprise-reclamation-request.md) as follows:

-   Pending
-   Pending evaluation
-   Complete

