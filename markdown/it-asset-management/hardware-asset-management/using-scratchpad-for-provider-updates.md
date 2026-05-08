---
title: Use the Scratchpad to complete your request fulfillment tasks
description: As a provider, use the Scratchpad feature of the Service Exchange application to send updates to the ServiceNow instance of your consumer while performing the request fulfillment tasks.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Zero Touch request flow, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Use the Scratchpad to complete your request fulfillment tasks

As a provider, use the Scratchpad feature of the Service Exchange application to send updates to the ServiceNow instance of your consumer while performing the request fulfillment tasks.

The Zero Touch request flow requires you to send Scratchpad updates to your consumer's ServiceNow instance when you complete the confirmation and shipment tasks successfully. Based on the updates that you send, the Zero Touch flow progresses on your consumer's ServiceNow instance.

You must include the code specific to your tasks in the **PSBScratchpadUtil** API. For more information, see Using the Scratchpad for Service Exchange tasks. Confirm that the Scratchpad codes associated with the tasks of your request fulfillment flow are in the following format.

## Sample code for request confirmation

```
var scratchPadJSON = {
  "orderStatus": "confirmed"
};
var value = JSON.stringify(scratchPadJSON); 
var rtGR = new GlideRecord("sn_sb_pro_provider_task"); 
rtGR.get(<ProviderTaskID>); 
if (rtGR.isValidRecord()) { 
  var util = new sn_sb_pro.PSBScratchpadUtil(); 
  util.update(rtGR, "confirmation", value); 
}

```

When you confirm a provider task, a Scratchpad update with the order status as **Confirmed** is sent to your consumer's ServiceNow instance.

## Sample code for shipment

```
var scratchPadJSON = {
"orderStatus": "partially_shipped / fully_shipped"
"orderLineItems" : 
  [{ 
    "status": "shipped",
    "trackingNumber": "123",
    "carrier": "C1",
    "modelNumber": 'MD322LL/A',
    "assetTag": 'P1000177',
    "serialNumber": 'P1000177'
  },{ 
    "status": "shipped",
    "trackingNumber": "123",
    "carrier": "C1",
    "modelNumber": 'MD322LL/A',
    "assetTag": 'P1000178',
    "serialNumber": 'P1000178'
  }
]
};

```

When you ship the requested items and confirm the shipment, a Scratchpad update with the following details are sent to your consumer's ServiceNow instance:

-   **Order status**: Depending on how the provider has shipped the assets in a request, the Order status can have the following values:

    -   **partially\_shipped**: Assets in the request are shipped through multiple shipments.
    -   **fully\_shipped**: All the assets in the request are shipped.
    For example, consider that a requester has requested for five assets. If you ship only three assets though a shipment, you should pass the **Order status** as **partially\_shipped**. When you ship the remaining two assets, you should pass the **Order status** as **fully\_shipped**.

-   **Tracking number**: Every shipment has a unique tracking number.
-   **Carrier**: The name of the carrier through which the provider shipped the assets.
-   **Model number**: Unique model number of the asset that is shipped.
-   **Asset tag**: Unique asset tag of the asset that is shipped.
-   **Serial number**: Serial number of the asset.

**Note:** The shipment update for consumable assets doesn't include Asset tag and Serial number details. If there are multiple shipments, the information of the asset in a shipment must be sent to your consumer's ServiceNow instance only once.

