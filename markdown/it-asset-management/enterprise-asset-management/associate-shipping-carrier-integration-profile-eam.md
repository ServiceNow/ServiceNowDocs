---
title: Associate a third-party shipping carrier with an integration profile in the Enterprise Asset Workspace
description: Associate a third-party shipping carrier with an integration profile so that you can successfully connect to that shipping carrier.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing enterprise asset shipments, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Associate a third-party shipping carrier with an integration profile in the Enterprise Asset Workspace

Associate a third-party shipping carrier with an integration profile so that you can successfully connect to that shipping carrier.

## Before you begin

Role required: sn\_eam.enterprise\_admin

## About this task

Each shipping carrier can be associated with only one active integration profile at a time. If any of your integration profiles are not already associated with a shipping carrier, you can view and take action on those integration profiles by using the Unmapped carrier profiles important action in the Inventory view of the Enterprise Asset Workspace.

## Procedure

1.  From the Enterprise Asset Workspace, open the Asset operations view.

2.  From the left navigation menu of the Asset operations view, navigate to **Shipment** &gt; **Carrier integration profiles**.

3.  Select the integration profile that you want to associate a shipping carrier with.

4.  On the integration profile record, select the **Shipping Carriers** tab.

5.  Associate a shipping carrier with the integration profile.

    -   To associate an existing shipping carrier with the integration profile, use the following steps:
        1.  Select **Add**.

            The Add carriers dialog box opens.

        2.  In the dialog box, search for and select the shipping carrier that you want to associate with the integration profile.

            **Note:** The dialog box displays only the shipping carriers that aren’t already associated with an integration profile.

        3.  Select **Add**.
    -   To associate a new shipping carrier with the integration profile, use the following steps:
        1.  Select **New**.
        2.  On the form, fill in the fields.

            |Field|Description|
            |-----|-----------|
            |Name|Name of the shipping carrier.|
            |Email|Email address of the shipping carrier.|
            |Integration profile|Integration profile that you are using to connect to the shipping carrier. This field populates automatically.|
            |Status|Status of the shipping carrier.|
            |Phone|Phone number of the shipping carrier.|
            |Website|Third-party website of the shipping carrier.|
            |Company|Company name of the shipping carrier, such as FedEx or UPS.|
            |Notes|Additional notes about the shipping carrier.|

        3.  Select **Save**.

## Result

The shipping carrier is associated with the integration profile.

**Parent Topic:**[Managing enterprise asset shipments](../concept/manage-shipments-eam.md)

