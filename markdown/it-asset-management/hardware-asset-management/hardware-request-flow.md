---
title: Use a hardware asset request flow
description: Use a hardware asset request flow for requesting, sourcing, and deploying hardware catalog items from the Service Catalog application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/hardware-asset-management/hardware-request-flow.html
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Use, Hardware Asset Management, IT Asset Management]
---

# Use a hardware asset request flow

Use a hardware asset request flow for requesting, sourcing, and deploying hardware catalog items from the Service Catalog application.

## Before you begin

Role required:

-   catalog\_admin
-   procurement\_admin

## About this task

Create a request for a hardware catalog item from the Service Catalog application. Associate the catalog item with the Standard Hardware Asset Request flow to trigger the flow.

The Workflow Studio application is used to create the Standard Hardware Asset Request flow to take you through the process of sourcing, procuring, and deploying your hardware catalog items. As the flow takes you through the various stages, the asset details are automatically updated. You can open the Standard Hardware Asset Request flow to view the status of the stages in the flow.

\[Omitted image "Hardware-asset-req-flow.png"\] Alt text: Hardware asset disposal flow

## Procedure

1.  Log in with credentials for the role of catalog\_admin and navigate to **Service Catalog** &gt; **Maintain Items**.

2.  Open the hardware catalog item and in the **Flow** field, select **Standard Hardware Asset Request**.

    If the **Flow** field isn’t visible, add it to the form layout by right-clicking the menu icon and navigating to **Configure** &gt; **Form layout**.

3.  Select **Save**.

    The Standard Hardware Asset Request flow is now associated with the hardware catalog item.

4.  Navigate to **Service Catalog** and select **Hardware**.

5.  Select your catalog item from the list.

6.  In the **Location** field, specify the location where the assets should be deployed.

    By default, this field is set to the location of the logged-in user. However, you can select a location from the list of available locations.

    **Note:** This field is available only for Hardware catalog items that are published from Hardware models after upgrading to Hardware Asset Management 8.0.0.

7.  In the **Quantity** field, specify the quantity of the assets and select **Order Now**.

8.  Log in with credentials for the role of procurement\_admin and open the new request.

9.  In the Requested Items related list, select the request item.

10. In the Requested Item form layout, select the **Flow Context** related link to view the current stage of the Standard Hardware Asset Request flow.

11. Select the **Catalog Tasks** related list to view the sourcing task for the request.

12. Open the catalog task and select **Source Request**.

13. In the Source Request form layout, select **Add Transfer Order** or **Add Purchase Order** to source the request via a transfer order or a purchase order.

    After you procure the catalog item,the Asset pick task is created for the Requested item only if the asset is sourced from the stockroom which has the Asset Pick task enabled. Otherwise the Deployment task is created for the Requested itemwithout the Asset pick task.For details, see [Enable the Asset pick task for your stockroom in the Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/enable-pick-task-for-stockroom-ham.md).

14. Select the Requested items related list and select the requested item.

15. Select the **Catalog Tasks** related list.

    -   If the Pick task is enabled for the source stockroom, complete the Asset pick task first and then complete the Deploy task.
    -   If the Pick task isn't enabled, complete the Deploy task.
16. Complete the Asset pick task using the Mobile Agent application.

    For details on completing this step, see [Manage hardware asset pick tasks using the Mobile Agent application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/manage-asset-pick-task-ham-mobile-app.md).

    The Deployment task is created for the requested item.

17. Close the Deployment task.

    In the Standard Hardware Asset Request flow, the action that is associated with deploying the assets is complete. The **State**, **Assigned**, **Installed**, **Location**, and **Assigned to** fields of asset are updated. The CI that is associated with the asset is also updated.


**Parent Topic:**[Using Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/using-ham-classic.md)

**Related topics**  


[Work with hardware normalization]()

[Manage asset bundles from your inventory]()

[Manage your inventory through pallet assets]()

[Manage loaner assets]()

[Donate assets to charity organizations]()

[Use Advanced Shipment Notification]()

[Manage RMA requests]()

[Create an inventory stock order request]()

[Create a disposal order]()

[Audit hardware asset inventory]()

[Request a Hardware Asset Refresh]()

[Manage your expiring contracts for leased hardware assets]()

[Reclaim hardware assets]()

[View RFID information of assets]()

[Manage the lifecycle of hardware models with calculated lifecycle templates]()

[Create an internal lifecycle in the Hardware Asset Workspace]()

[Receive asset warranty details from Lenovo]()

[Manage stockrooms]()

[Track shipments using the integration framework]()

[Track asset location using indoor maps]()

[Assess performance of Hardware Asset Management]()

[Manage refresh of assets using Zero Touch Refresh]()

[Configure the Total Cost of Ownership of assets]()

[Manage Hardware Asset Management subscriptions]()

[Manage repair of defective assets in your stockroom in the Hardware Asset Workspace]()

[Manage picking hardware assets within your stockroom for Hardware Asset Management workflows]()

[Manage hardware asset tasks using the Mobile Agent application]()

[Manage asset put away using the Hardware Asset Workspace]()

[Audit your hardware assets by using Asset Attestation]()

[Acknowledge receipt of assets on the Employee Center portal]()

[Update associated Decision tables for HAM flows]()

