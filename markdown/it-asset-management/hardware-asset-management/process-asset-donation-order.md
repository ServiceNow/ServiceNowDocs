---
title: Process an Asset Donation Order
description: Process an Asset Donation Order to prepare and send assets to a charity organization.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Donate assets to charity organizations, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Process an Asset Donation Order

Process an Asset Donation Order to prepare and send assets to a charity organization.

## Before you begin

Role required: asset

## About this task

You can cancel an Asset Donation Order until it reaches the transit stage in the workflow. After your Asset Donation Order reaches the Confirmation stage, you can't cancel it.

**Note:** You can process Asset Donation Orders only in Hardware Asset Workspace and not in Hardware Asset Management Core UI.

## Procedure

1.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Inventory**.

2.  Open the **Donation orders** tab.

    A list of asset donation orders is shown.

3.  Select an Asset Donation Order that is in the **Scheduling** stage.

4.  Add assets to the Asset Donation Order.

    1.  Open the **Planned Assets** tab.

    2.  Select **Add**.

    3.  In the Add assets pop-up window, select assets that are part of the domain whose state is In stock and substate is Pending donation, and then select **Add**.

        Use the filter to search for the desired assets.

        The assets that you added are shown under the Planned Assets tab.

5.  Prepare the assets for donation and provide a date to pick up the assets.

    1.  Open the **Asset Donation Tasks** tab.

    2.  Select the Prepare assets and provide Scheduled date task.

    3.  In the Planned Assets related list, select the assets that you want to prepare and then select **Prepare**.

        **Note:** You can configure subflows for asset preparation tasks based on your needs and the type of assets to be donated. For example, you can configure Prepare asset tasks for a data storage asset that needs data wiping or a hardware asset that needs packaging before it’s donated.

        The stage of the planned assets changes to Prepared.

    4.  On the Schedule details form, in the **Scheduled date** field, select a date for pick up.

    5.  Select **Close task**.

        The state of the task changes to Closed complete, and the Select the assets departing for donation task is created as an asset donation task.

6.  Select the assets to be sent.

    1.  Open the Select the assets departing for donation task.

    2.  In the Planned Assets related list, select the assets that you want to send from the stockroom and select **Depart**.

        The stage of the planned assets changes from Prepared to In transit. The state of the assets changes to In transit and the Substate changes to Pending donation.

7.  Provide the name of the vendor to pick up the assets and the shipment tracking details.

    1.  Open the Details tab.

    2.  On the Schedule details form, specify the following:

        1.  In the **Pickup contact name** field, enter the name of the vendor to pick up the assets for donation.
        2.  \(Optional\) In the **Shipping carrier** field, select your shipping carrier.
        3.  \(Optional\) In the **Tracking number** field, enter the tracking number for the shipment.
        **Note:** The Shipping carrier and Tracking number fields are used to track shipments from the Shipment list in the Asset operations view of the Hardware Asset Workspace. For details, see [View hardware asset shipment details](view-hardware-asset-shipments.md).

    3.  Select **Close task**.

        The State of the task changes to Closed complete. Confirmation from the charity organization task is created under the assets donation tasks.

8.  Confirm donation of the assets.

    1.  Select the Confirmation from charity organization task.

    2.  In the Planned assets related list, select the assets and then select **Confirm Donation**.

        The stage of the assets changes to Completed. The state of the assets changes to Retired and the substate changes to Donated.

9.  Attach the donation documentation from the charity organization to the Asset Donation Order record.

    1.  Select the Confirmation from charity organization task.

    2.  In the Details related list, select the Attachment icon ![](../image/paper-clip-icon.png).

    3.  Select the document.

    4.  In the Certificate of donation list, select **Yes**.

        The state of the Asset Donation Order is set to Completed.

    5.  Select **Close task**.


## Result

All the asset donation tasks are in the Closed Complete state and the Asset Donation Order stage changes to Completed.

**Parent Topic:**[Donate assets to charity organizations](../concept/donate-asset-to-charity-organizations.md)

**Related topics**  


[Create an Asset Donation Order](create-asset-donation-order.md)

[Approve or reject an Asset Donation Order](approve-reject-asset-donation-order.md)

[Add a charity organization for donating assets](add-charity-org.md)

