---
title: Use an enterprise asset request flow
description: Use an enterprise asset request flow for requesting, sourcing, and deploying catalog items from the Service Catalog application.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Using Service Catalog for Enterprise Asset Management requests and flows, Enterprise Asset Management, IT Asset Management]
---

# Use an enterprise asset request flow

Use an enterprise asset request flow for requesting, sourcing, and deploying catalog items from the Service Catalog application.

## Before you begin

Before requesting for an enterprise asset, ensure that you have already created a model for that asset in the Enterprise Asset Workspace and published that model to the Service Catalog application.

Role required:

-   catalog\_admin
-   procurement\_admin
-   sn\_eam.enterptrise\_asset\_manager
-   sys\_admin

## About this task

Create a request for an enterprise catalog item from the Service Catalog application. Associate the catalog item with the Standard Enterprise Asset Request flow to trigger the flow.

The Workflow Studio application is used to create the Standard Enterprise Asset Request flow to take you through the process of sourcing, procuring, and deploying your enterprise catalog items. As the flow takes you through the various stages, the asset details are automatically updated. You can open the Standard Enterprise Asset Request flow to view the status of the stages in the flow.

## Procedure

1.  Log in with credentials for the role of catalog\_admin and navigate to **Service Catalog** &gt; **Maintain Items**.

2.  Open the enterprise catalog item and in the **Flow** field, select **Standard Enterprise Asset Request**.

    If the **Flow** field is not visible, add it to the form layout by right-clicking the menu icon and navigating to **Configure** &gt; **Form layout**.

3.  Select **Save**.

    The Standard Enterprise Asset Request flow is now associated with the enterprise catalog item.

4.  Navigate to the Service Catalog application.

5.  Login with credentials for the role of sys \_admin role and add the **Enterprise Assets** catalog.

    The **Enterprise Assets** catalog is not on the Service Catalog page by default. To add this catalog, select the Add Content icon ![Add Content icon](../../hardware-asset-management/image/add_content_icon.png) \) beside the search catalog bar and then select **Enterprise Assets**

6.  Login with credentials for the role of sn\_eam.enterptrise\_asset\_manager and select the **Enterprise Assets** catalog.

    The Enterprise Assets page opens.

7.  Select your catalog item from the list.

    The catalog item page opens.

8.  In the **Location** field, select the location in which you want to deploy the catalog item.

9.  Select **Order Now**.

10. Log in with credentials for the role of procurement\_admin and open the new request.

11. In the Requested Items related list, select the request item.

12. Select the **Catalog Tasks** related list to view the sourcing task for the request.

13. Open the catalog task and select **Source Request**.

14. In the Source Request form layout, select **Add Transfer Order** or **Add Purchase Order** to source the request via a transfer order or a purchase order.

    After you procure the catalog item,the Asset pick task is created for the Requested item only if the asset is sourced from the stockroom that has the Asset pick task enabled. Otherwise the Deployment task is created for the Requested itemwithout the Asset pick task.For details, see [Enable the Asset pick task for your stockroom in the Hardware Asset Workspace](../../hardware-asset-management/task/enable-pick-task-for-stockroom-ham.md).

15. Select the Requested items related list and select the requested item.

16. Select the **Catalog Tasks** related list.

    -   If the Pick task is enabled for the source stockroom, complete the Asset pick task first and then complete the Deploy task.
    -   If the Pick task isn't enabled,complete the Deploy task.
17. Complete the Asset pick task using the Mobile Agent application.

    For details on completing this step, see [Manage enterprise asset pick tasks using the Mobile Agent application](../concept/manage-asset-pick-task-eam-mobile-app.md).

    The Deployment task is created for the requested item.

18. Enter a value in the **Assigned to** field, and select **Deploy Asset**.

    If it's a serialized asset, it's marked as **In use** state. If it’s a consumable asset, it’s marked as **Consumed** state. In the Standard Enterprise Asset Request flow, the action that is associated with deploying the assets is now complete.


