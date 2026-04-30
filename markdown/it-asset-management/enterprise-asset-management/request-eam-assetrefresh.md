---
title: Request an enterprise asset refresh
description: Use the Enterprise Asset Refresh flow to track the assets that are nearing the end of their life cycle and replace them with new assets.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Service Catalog for Enterprise Asset Management requests and flows, Enterprise Asset Management, IT Asset Management]
---

# Request an enterprise asset refresh

Use the Enterprise Asset Refresh flow to track the assets that are nearing the end of their life cycle and replace them with new assets.

## Before you begin

Role required: inventory\_user

## About this task

When assets get old, their maintenance costs and risks of failure increase, while their performance decreases. You can choose to replace old assets with the same or different models of newer assets. After your Enterprise Asset Refresh request is approved, the Enterprise Asset Refresh flow takes you through sourcing and triggers the Enterprise Asset Refresh Line flow. The Enterprise Asset Refresh Line flow uses Refresh Line tasks to take you through the steps of preparing the new asset, scheduling it for delivery, deploying it, and reclaiming the aged asset.

The Workflow Studio application is used to create the Enterprise Asset Refresh flow and the Enterprise Asset Refresh Line flow.

## Procedure

1.  Navigate to the Service Catalog application.

2.  Login with credentials for the role of sys \_admin role and add the **Enterprise Asset Lifecycle** catalog.

    The **Enterprise Asset Lifecycle** catalog is not on the Service Catalog page by default. To add this catalog, select the Add Content icon ![Add Content icon](../../hardware-asset-management/image/add_content_icon.png)\) beside the search catalog bar and then select **Enterprise Asset Lifecycle**.

3.  Login with credentials for the role of sn\_eam.enterptrise\_asset\_manager and select the **Enterprise Asset Lifecycle** catalog.

    The Enterprise Asset Lifecycle page opens.

4.  Navigate to **Service Catalog** &gt; **Enterprise Asset Lifecycle**.

    The **Enterprise Asset Lifecycle** catalog is not on the Service Catalog page by default. To add this category, select the add content icon \(![Add content icon.](../../hardware-asset-management/image/add_content_icon.png)\) beside the search catalog bar and then select **Enterprise Asset Lifecycle**.

5.  Open **Enterprise Asset Refresh Order**.

6.  If you want to replace all the aged enterprise assets with the same model of new enterprise assets, do the following:

    1.  Select **Single model** from the **Type of refresh list** field.

    2.  On the form, fill in the fields.

<table id="table_mzn_b4q_2nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Location

</td><td>

Physical location of the aged enterprise assets.

</td></tr><tr><td>

Replacement model

</td><td>

New enterprise asset model that you want to replace the aged enterprise assets with.

</td></tr><tr><td>

Assets

</td><td>

Aged enterprise assets that you want to replace. You can use a filter to search for enterprise assets that you want to replace.

</td></tr><tr><td>

Available

</td><td>

Displays only those assets for which the **Eligible for Refresh** check box on the Asset page is selected. To view all assets that are nearing their end of life, execute the condition `Eligible for refresh is false`.**Note:** For details on the **Eligible for Refresh** check box, see [Asset fields for enterprise assets](../reference/asset-fields-eam.md).

</td></tr></tbody>
</table>7.  If you want to replace the aged hardware assets with different models of new hardware assets, do the following:

    1.  Select **Multi model** from the **Type of refresh** field.

    2.  Select **Add**.

    3.  For each new enterprise asset that you want to use, add a row to enter the enterprise model.

        **Note:** You can create 50 rows. You cannot create multiple rows for the same aged hardware asset that you want to replace.

8.  Select **Order Now**.

    An Order status page appears and displays the details of the order. A request is created to source the new enterprise assets and to replace the aged enterprise assets. The Request form shows the total price of all the new enterprise asset models.


-   **[Replace aged enterprise assets](replace-aged-enterprise-assets.md)**  
Replace aged enterprise assets by sourcing new enterprise assets.

**Parent Topic:**[Using Service Catalog for Enterprise Asset Management requests and flows](../concept/using-service-catalog-eam-requests-flows.md)

