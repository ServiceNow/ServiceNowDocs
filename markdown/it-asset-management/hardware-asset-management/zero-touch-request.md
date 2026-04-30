---
title: Zero Touch request flow
description: Fulfill the hardware requests of your employees through an external provider with minimal intervention by using the Zero Touch request flow.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Zero Touch request flow

Fulfill the hardware requests of your employees through an external provider with minimal intervention by using the Zero Touch request flow.

## Zero Touch request flow requirements

The Zero Touch request flow has the following basic requirements:

1.  Your organization and the provider must be on the ServiceNow Cloud.
2.  The ServiceNow Service Exchange application must be configured on the ServiceNow instance.
3.  Your provider must have published the Remote catalog items or Remote record producers.

## Zero Touch request workflow

1.  An employee of your organization submits a catalog request for a catalog item associated with the Zero Touch request flow.

    A catalog request is created with the **Request state** as **Pending Approval**.

2.  The approver reviews the catalog request and performs either of the following tasks:
    -   Rejects the catalog request: The **Request state** changes to **Closed Rejected** and the **Stage** of the requested item changes to **Closed incomplete**.
    -   Approves the catalog request: The **Request state** changes to **Approved** and the **Stage** of the Requested item changes to **Pending Confirmation**.

        **Note:** If a requester who doesn't have access to the remote record producer submits a catalog request, the requested item is marked as **Closed incomplete**.

3.  After the catalog request is approved, the request goes through the following changes:
    1.  The request is sent to the provider based on the Remote record producer configured in the catalog item mapping.
    2.  The **Stage** of the requested item changes to **Pending confirmation** on the ServiceNow instance of your organization.
4.  The provider sends a Scratchpad update confirming the order to your ServiceNow instance. The **Stage** of the requested item changes to **Pending shipment**.
5.  The provider ships the asset to your employee and sends a Scratchpad update with the shipment details to your ServiceNow instance.

    The following events happen when the provider ships the asset:

    -   An asset with the serial number and asset tag specified by the provider is assigned to the employee.

        **Note:** An email notification is sent to the asset managers in the following scenarios to take necessary actions:

        -   An asset record with the serial number provided by the provider exists on your ServiceNow instance.
        -   The model number provided by the provider isn't available on your ServiceNow instance.
        -   The asset that is shipped is a consumable.
    -   Based on the tracking number and shipping carrier details that the provider specified in the Scratchpad update, a unique shipment record is created for the shipment. You can view the shipment records with the associated assets in the Assets operations view of the Hardware Asset Workspace. For more details, see [View hardware asset shipment details](../task/view-hardware-asset-shipments.md).
    When shipping an asset bundle, the provider can choose to ship the assets fully through a single shipment or partially through multiple shipments. Only when the assets are fully shipped, the **Stage** of the requested item changes to **Pending receive**.

6.  The employee acknowledges the receipt of the asset on a mobile device. The Stage of the requested item changes to Complete.

    **Note:** Receipt of the consumable asset can't be confirmed on a mobile device. The asset manager takes the necessary actions based on the email notifications received and confirms on behalf of the employee.


For more details on creating and fulfilling hardware asset requests through the Zero Touch request flow, see [Manage hardware asset requests using the Zero Touch request flow](managing-standard-hw-req-ztr.md).

