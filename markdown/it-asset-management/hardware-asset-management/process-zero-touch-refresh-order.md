---
title: Fulfill a Zero Touch Refresh Fulfillment Request
description: As a provider, ship a replacement asset requested through a Zero Touch Refresh Fulfillment Request to the requester.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Manage refresh of assets using Zero Touch Refresh, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Fulfill a Zero Touch Refresh Fulfillment Request

As a provider, ship a replacement asset requested through a Zero Touch Refresh Fulfillment Request to the requester.

## Before you begin

The Service Exchange configuration necessary for the Zero Touch Refresh flow must have been set up. For more details, see [Service Exchange configuration for Zero Touch Refresh](../concept/service-bridge-config-ztr.md).

Role required: admin, asset, procurement\_user, or inventory\_user

## About this task

When an employee submits a Zero Touch Refresh request on the ServiceNow® instance of your customer, a corresponding Zero Touch Refresh Fulfillment Request is created on your ServiceNow® instance.

## Procedure

1.  Log in to your ServiceNow® instance.

2.  Navigate to **All** &gt; **Zero Touch Refresh Fulfillment Requests**.

3.  Select a request that is in the Requested state.

4.  Review the details on the Zero Touch Refresh Fulfillment Request form.

    The Customer request number field shows the corresponding Zero Touch Refresh request number. The fields in the Shipment details tab and the Return shipment details tab are populated with the details specified in the Zero Touch Refresh request.

5.  Confirm the Zero Touch Refresh Fulfillment Request.

    1.  In the **State** field, select **Order confirmed**.

    2.  Select **Save**.

6.  Ship the replacement asset to the requester or to the stockroom.

    1.  Enter the asset information in the **Asset tag** and **Serial number** fields.

    2.  In the **Shipment details** tab, enter values in the **Tracking number** and **Carrier** fields.

    3.  In the **Return shipment details** tab, enter values in the **Tracking number** and **Carrier** fields.

    4.  In the **State** field, select **Shipped**.

    5.  Select **Save**.

    6.  In the shipment, include a box that the employee can use to return the old asset with an address label made out for the stockroom.

    7.  Ship the new asset to the requester or to the stockroom location where the requester can pick up the asset.


## Result

An asset with the serial number and asset tag specified in the Zero Touch Refresh Fulfillment Request is assigned to the employee.

**Parent Topic:**[Manage refresh of assets using Zero Touch Refresh](../concept/refresh-hardware-uisng-ztr.md)

**Related topics**  


[Configure replacement models for a refresh model](create-replacement-model.md)

[Request a hardware asset refresh through Zero Touch Refresh](create-zero-touch-refresh-request.md)

[Process a Zero Touch Refresh request](process-zero-touch-asset-request.md)

[Acknowledge receipt of an asset on a mobile device](receive-assets-from-ztr.md)

[Acknowledge receipt of an asset through the Core UI](acknowledge-asset-core-ui.md)

