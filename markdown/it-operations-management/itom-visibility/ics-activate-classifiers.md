---
title: Enable discovery with ITOM Content Service
description: Review the ITOM Content Service suggestions for application discovery and activate the discovery classifiers to enable the creation of configuration items.
locale: en-US
release: xanadu
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ITOM Content Service, ITOM Visibility, IT Operations Management]
---

# Enable discovery with ITOM Content Service

Review the ITOM Content Service suggestions for application discovery and activate the discovery classifiers to enable the creation of configuration items.

## Before you begin

Ensure that the following application and plugin are installed:

-   ITOM Content Service \(sn\_smart\_content\)
-   Discovery Admin Workspace \(com.snc.itom.daw\)

Ensure that ITOM Content Service is active. For more information, see [Share data on ITOM Content Service](share-data-itom-content-service.md).

Role required: discovery\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Content 360**.

2.  Select the **Content service suggestions** tile.

3.  Manually sync with suggestions from your system by selecting **Sync candidates**.

    **Note:** If a message appears about the application scope, select **OK** to exit the message. Then, change the scope by selecting the application scope icon \(![Application scope icon](../../agent-client-collector/image/application-scope-icon.png)\) and selecting **Global**.

4.  In the Sync candidates confirmation window, select **Yes**.

5.  Review the Content Service suggestions for discovery by product.

    -   To filter the list, select the products from the **Content service suggestions** tab.
    -   To review a product's description and details, select the link from the **Name** column.
6.  Select the product you want to enable discovery for.

7.  Activate discovery classifiers by product categories.

    **Note:** The number of classifiers that will be activated is indicated in the **Activate** button.

    -   To enable the discovery by product categories, select the product categories check boxes, select the check box next to the **Name** column, and select **Activate**.
    -   To enable the discovery by individual products, select the product from the **Name** column and select **Activate**.

## Result

The new configuration items are added to the CMDB the next time Discovery runs a schedule. The Discovery Admin Workspace then lists the added CIs and removes them from the suggested applications list.

**Related topics**  


[ITOM Content Service](../concept/discovery-content-services.md)

[Discovery Admin Workspace](../concept/discovery-admin-workspace.md)

