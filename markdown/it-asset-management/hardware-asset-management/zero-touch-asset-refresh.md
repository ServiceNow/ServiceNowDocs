---
title: Zero Touch Refresh
description: Use the Zero Touch Refresh flow to fulfill employee hardware refresh requests through an external vendor without having to maintain new assets in the local stockroom.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Zero Touch Refresh

Use the Zero Touch Refresh flow to fulfill employee hardware refresh requests through an external vendor without having to maintain new assets in the local stockroom.

The various stages in the asset refresh process are as follows:

1.  An employee of your organization submits a request for refresh of the hardware asset.

    The Request confirmation task is created when the Zero Touch Refresh request is approved. The state of this task changes to Closed automatically when the provider confirms the request.

2.  Provider ships the new asset to the employee.

    **Note:** A provider can fulfill a Zero Touch Refresh request by using the Asset Management application.

    The following tasks are created:

    1.  Request shipment: This task is created when the provider confirms the Zero Touch Refresh request. The state of this task changes to Closed automatically when the provider ships the new asset.

        The following happen when the provider ships the asset:

        -   An asset with the serial number and asset tag specified by the provider is assigned to the employee.
        -   Based on the refresh method that the employee selected in the Zero Touch Refresh request, email notifications with details of the new replacement asset that is shipped are sent as follows:
            -   When the asset is shipped to the employee, an email notification is sent to all users with the asset role.
            -   When the asset is shipped to the stockroom, an email notification is sent to all users with the asset role and also the stockroom manager of the selected stockroom from where the employee will pick up the new asset.
        -   Based on the tracking number and shipping carrier details that the provider specified in the request, unique shipment records are created for the shipments of the replacement asset and the old asset. When the same tracking number is provided for both the shipments, a single shipment record is created. You can view the shipment records with the associated assets in the Assets operations view of the Hardware Asset Workspace. For more details, see [View hardware asset shipment details](../task/view-hardware-asset-shipments.md).
    2.  Ready for pickup: This task is created only for the Pickup refresh method in which the provider ships the new asset to the stockroom from where the employee picks up the asset.
    3.  Receive asset: This task is created as follows:
        -   For the Ship refresh method, when the provider ships the asset to the employee.
        -   For the Pickup refresh method, when the Ready for pickup task is closed.
    4.  Receive return asset: This task is created when the provider ships the new asset.
3.  Employee confirms receipt of the new asset.
4.  Employee returns the old asset to the stockroom in the labeled box shipped by the provider.
5.  Inventory manager confirms that the old asset was received and evaluates it.

**Note:** The Zero Touch Refresh flow requires support from an external provider and is pre-configured to integrate with Insight.

The Zero Touch Refresh flow has the following requirements:

-   The employee's organization and the provider must be on the same ServiceNow Cloud.
-   The Service Exchange application must be configured on the ServiceNow instance of the provider and the employee's organization.

For more details, see [Manage refresh of assets using Zero Touch Refresh](refresh-hardware-uisng-ztr.md).

