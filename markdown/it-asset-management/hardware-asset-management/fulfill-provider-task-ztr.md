---
title: Fulfill a provider task
description: As a provider, ship the asset requested through the Zero touch request flow to the requester.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Manage hardware asset requests using the Zero Touch request flow, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Fulfill a provider task

As a provider, ship the asset requested through the Zero touch request flow to the requester.

## Before you begin

1.  The Service Exchange configuration necessary for the Zero Touch Refresh flow must have been set up. For more details, see [Configure Service Exchange for the Zero Touch request flow](../concept/service-bridge-for-ztreq.md).
2.  The Scratchpad must have been configured for the confirmation and shipment tasks involved in your request fulfillment flow. For more information, see [Use the Scratchpad to complete your request fulfillment tasks](../concept/using-scratchpad-for-provider-updates.md).

Role required: Roles are provider-specific

## About this task

When an employee places an order for the catalog item associated with the Zero Touch request flow on your consumer's ServiceNow® instance, a corresponding Provider task is created on your ServiceNow® instance. The provider task triggers a request fulfillment flow on your ServiceNow® instance. As the provider task moves through various stages in the fulfillment flow, the information is sent to your consumer's instance through the Scratchpad updates.

## Procedure

1.  Log in to your ServiceNow® instance.

2.  Navigate to **All** &gt; **Service Bridge Provider** &gt; **Open Records** &gt; **Provider Tasks**.

3.  Select a provider task that is in the Received state.

4.  Review the details on the Provider task form.

    The Variables section provides details that the requester provided on the Service Catalog request.

5.  Confirm the provider task by sending a Scratchpad update to your consumer's ServiceNow® instance.

6.  Ship the assets requested in the provider task and send a Scratchpad update with the shipment details to your consumer's ServiceNow® instance.

    The following shipment details are included in the Scratchpad:

    -   Order status: Order status could be either **fully\_shipped** or **partially\_shipped**.
    -   Tracking number: Unique tracking number for the shipment.
    -   Model number: Unique model number of the asset that is shipped.
    -   Asset tag: Unique asset tag of the asset that is shipped.
    -   Serial number: Serial number of the asset.

## Result

An asset with the serial number and asset tag specified in the Scratchpad is assigned to the requester.

