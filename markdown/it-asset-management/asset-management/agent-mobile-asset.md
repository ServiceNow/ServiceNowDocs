---
title: ServiceNow Agent app
description: Use the ServiceNow Agent app to create assets, look up assets, and receive assets from a purchase order.Use the ServiceNow Agent app to create an asset record by scanning the asset.Search for an asset record in your ServiceNow instance by scanning the asset.Scan assets from a purchase order \(PO\) to verify that you received all assets from the order.Use the ServiceNow Agent app to scan, verify, and depart your assets for disposal.
locale: en-US
release: zurich
product: Asset Management
classification: asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Mobile app for Hardware Asset Management, Use, Asset Management, IT Asset Management]
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

5.  If you only need to receive a single purchase, on the Receive form, scan the QR code for either the asset tag or serial number.

6.  If you need to receive multiple purchases, on the Receive form, tap **Scan next item** until you've scanned all of your purchases.

7.  Tap **Submit**.


### Result

The purchase order is marked as received.

## Verify and depart your assets for disposal

Use the ServiceNow Agent app to scan, verify, and depart your assets for disposal.

### Before you begin

To verify an asset using the ServiceNow Agent app, make sure that a Disposal order exists in your Hardware Asset Management instance.

Role required: asset

### About this task

After a Disposal order is initiated for your asset, use the ServiceNow Agent app to scan, verify, and depart the asset. You do not have to manually verify and depart your assets.

On the app, you can use the same functionalities when you are offline. For more information, see [Offline mode](https://www.servicenow.com/docs/access?context=mobile-offline-mode&version=zurich&pubname=zurich-mobile&ft:locale=en-US).

### Procedure

1.  Navigate to **All** &gt; **Asset** &gt; **Asset disposal**.

    The **Verification** tab shows the list of verification tasks, while the **Departure** tab shows the list of departure tasks. These tasks are for the assets that are present in a particular asset location for disposal.

2.  Scan and verify your assets in one of the following ways.

    -   Swipe a verification task to the left.
    -   Tap a verification task to open it and then tap **Scan**.
    You can scan multiple assets together. After you open a verification task, the verification task shows the number of assets that are verified, not verified, or expected to be verified. Click **Expected**, **Verified**, or **Not verified** to view the respective types of assets.

    Here is an example of a **Verification** tab that shows expected, verified, and not verified assets.

    ![Verification tab.](../../hardware-asset-management/image/expected-assets.png)

3.  Tap **Review** &gt; **Submit**.

    A pop-up message appears and shows the successful verification of the scanned assets. The lists of verified and not verified assets are updated.

4.  Once you scan all the assets, tap **Complete** to close the verification task.

    If there are still some assets left for scanning and you click **Complete**, then a pop-up window appears to confirm if you still want to close the task. If you tap **Complete**, the task is closed.

5.  Enter the vendor details and the scheduled date by using your Hardware Asset Management instance.

    See [Create a disposal order](../../hardware-asset-management/task/create-disposal-order.md).

    After you enter the vendor details and close the Schedule Pickup task from your Hardware Asset Management instance, the **Departure** tab shows the list of departure tasks to process.

6.  Scan and depart your assets in one of the following ways.

    -   Swipe a departure task to the left.
    -   Tap a departure task to open it and then tap **Scan**.
    You can scan multiple assets together. After you open a departure task, the departure task shows the number of assets that are departed, not departed, or expected to be departed. Click **Expected**, **Departed**, or **Not departed** to view the respective types of assets.

7.  Tap **Review** &gt; **Submit**.

    A pop-up window appears and shows the successful departure of the scanned assets. The lists of departed and not departed assets are updated.

8.  Once you scan all the assets, tap **Complete** to close the departure task.

    If there are still some assets left for scanning and you click **Complete**, then a pop-up window appears to confirm if you want to close the task. If you tap **Complete**, the task is closed.


