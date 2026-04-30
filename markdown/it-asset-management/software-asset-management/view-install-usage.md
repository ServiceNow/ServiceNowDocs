---
title: View license usage for your installations
description: Track your installation to license journey by connecting software installations to the licenses consumed and identifying statuses such as licensed, unlicensed, ignored, or requiring action.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# View license usage for your installations

Track your installation to license journey by connecting software installations to the licenses consumed and identifying statuses such as licensed, unlicensed, ignored, or requiring action.

## Before you begin

Role required: sam\_manager

## Procedure

1.  Navigate to **Software Asset Workspace** &gt; **License operations** &gt; **Products with installs**.

    ![Products with installs](../image/products-with-installs.png)

    The preceding page showcases all your products with installations and offers a high-level overview of how these installations are being used and licensed.

2.  Select a product to open the Details page.

    ![SQL Server details](../image/sqlserver-product-install-details.png)

3.  Select **License usage**.

    ![License usage node map](../image/license-usage-node-map.png)

    The License use analysis page for the product opens displaying a four-level node map that illustrates how the licenses are being used.

    You can also access the License use analysis page from the Publisher details page by selecting **Product install analysis** for a publisher, selecting a product, and then selecting **License usage**.

4.  View the four-level node map to understand the license usage for the product.

    -   The highest level in the node map represents the product.
    -   The second-level features nodes for different product versions and editions, with each version-edition combo having its own node.
    -   The third level nodes indicate the licensing status of installations, such as licensed, unlicensed, requiring action, and ignored.
    -   The fourth level nodes display the licensing results for installation groups, showing which licenses are in use.
    You can select a node to delve deeper into the software installation lists and examine individual installation records.

    The top-right corner of the node map shows the reconciliation number that generated the current node map, along with the timestamp of the last reconciliation run. If reconciliation is executed with domain separation settings enabled, multiple node maps are displayed.

5.  Select the Export map icon on the right side of the page to download this node map as an image.


**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)

