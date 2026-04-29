---
title: Employee off-boarding process for asset reclamation
description: Coordinate an employee's off-boarding process via a workflow that lets you request, assess, and remove assets.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Employee off-boarding process for asset reclamation

Coordinate an employee's off-boarding process via a workflow that lets you request, assess, and remove assets.

The Software Asset Management off-boarding process entails the return of all software licenses assigned to the employee. Additionally, all software installations are removed from the devices, all user allocations are removed, and access to SSO, SAP, and Citrix products is revoked.

When an employee leaves an organization or moves to a different role, retrieving the assets assigned to the employee necessitates extensive coordination between the Human Resources department and the asset manager. You can create an off-boarding catalog request, which initiates a prescriptive workflow to efficiently retrieve assets and restock them in the inventory, reassign them, send them for repair, or dispose as required.

**Note:** For information on the Hardware Asset Management asset reclamation process, see [Asset reclamation](../../hardware-asset-management/concept/reclaim-asset.md#).

You can create an asset reclamation request via the Service Catalog. Once the request is created, reclamation line items are created that comprise of a series of tasks. These tasks can only be accessed and performed only by the sam\_user role. Once all the tasks are closed, the reclamation line item is complete. After all the reclamation line items are complete, the catalog request is also completed. For information on creating an off-boarding catalog request, see [Create a catalog request to reclaim assets](../task/create-catalog-req-offboardingsam.md).

**Note:** Software reclamation line items of the type Device Reclamation are created for each device that is returned, provided the device has software installations on it and that device was selected in the Reclaim Asset form. An additional software reclamation line item of the type User Reclamation is created if the **Employee Separation** check box was selected in the Reclaim Asset form.

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

