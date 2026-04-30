---
title: ServiceNow Agent app
description: Use the ServiceNow Agent app to create assets, look up assets, and receive assets from a purchase order.Use the ServiceNow Agent app to create an asset record by scanning the asset.Search for an asset record in your ServiceNow instance by scanning the asset.Scan assets from a purchase order \(PO\) to verify that you received all assets from the order.
locale: en-US
release: xanadu
product: Asset Management
classification: asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Mobile app for Hardware Asset Management, Asset Management, IT Service Management]
---

# ServiceNow Agent app

Use the ServiceNow Agent app to create assets, look up assets, and receive assets from a purchase order.

**Parent Topic:**[Mobile app for Hardware Asset Management](../../../administer/mobile-my-asset/concept/mobile-my-asset.md)

**Related topics**  


[Now Mobile app](now-mobile-asset.md)

## Create an asset

Use the ServiceNow Agent app to create an asset record by scanning the asset.

### Before you begin

Download the ServiceNow Agent app from Apple App Store or Google Play Store.

Role required: asset

The Procurement plugin \(com.snc.procurement\) must be installed to get the procurement features in ServiceNow Agent app.

### Procedure

1.  Navigate to **Asset** and tap **Create Asset**.

    ![Agent Mobile Asset home screen](../image/AgentAssetHome.png)

2.  Scan the asset serial number or asset tag, then tap **Search**.

    If the asset exists in your ServiceNow instance, an asset record is displayed. This information is to ensure that you don't create duplicate asset records.

3.  To update an existing asset, select the asset and then tap **Update Asset**.

4.  If no existing asset record is found, tap the action icon in the upper right and select **Create Asset**.

5.  Scan or enter values for the **Asset Tag**, **Serial Number**, **Model** \(non-software\), **Stockroom**, **State**, and **Substate** fields.

6.  Tap **Submit** to create the asset.


## Asset lookup

Search for an asset record in your ServiceNow instance by scanning the asset.

### Before you begin

Role required: asset

### Procedure

1.  Navigate to **Asset** and tap **Asset lookup**.

2.  Scan the asset tag, then tap **Search**.

3.  An asset record is displayed if the asset exists in your ServiceNow instance.

    You can select the existing asset to update it or to create an incident related to it.


## Receive assets from a purchase order

Scan assets from a purchase order \(PO\) to verify that you received all assets from the order.

### Before you begin

Role required: procurement\_admin or procurement\_user

### Procedure

1.  Navigate to **Procurement** and tap **POs Next 30 Days**.

2.  Select a purchase order.

3.  Tap **Related list**.

4.  Tap the **PO Line Items** asset that you ordered and swipe **Receive** to receive the asset.

    ![Swipe Receive on the Purchase Order Line Items page](../../../administer/mobile-my-asset/image/receive-asset.png)

5.  If you only need to receive a single purchase, on the Receive form, scan the QR code for either the asset tag or serial number.

6.  If you need to receive multiple purchases, on the Receive form, tap **Scan next item** until you've scanned all of your purchases.

7.  Tap **Submit**.


### Result

The purchase order is marked as received.

