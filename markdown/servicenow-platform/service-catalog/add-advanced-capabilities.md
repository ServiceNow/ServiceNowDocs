---
title: Add advanced capabilities to a catalog item
description: Add advanced capabilities, such as catalog client scripts, data lookup rules, and advanced reference qualifiers to a catalog item.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Edit a catalog item in Catalog Builder, Creating or editing catalog item template, Catalog Builder, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Add advanced capabilities to a catalog item

Add advanced capabilities, such as catalog client scripts, data lookup rules, and advanced reference qualifiers to a catalog item.

## Before you begin

Role required: catalog\_admin or admin

## Procedure

1.  Add advanced capabilities to a catalog item using any of these methods.

    -   Using the **Edit in advanced view** button.

        1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Builder**.
        2.  Select the **Catalog items** tab.
        3.  Select the catalog item for which you want to add advanced capabilities or features.
        4.  Select **Edit in advanced view**.
        **Note:** If you have the catalog item wizard open, and you want to edit it in advanced view, select the more actions icon \(![More Action icon](../image/more-actions-ne-icon.png)\) on the wizard, and select **Edit in advanced view**.

    -   Using the **Edit checked out item in advanced view** related link.
        1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Items**.

            **Note:**

            -   The checked out item icon \(![Checked out item icon.](../image/checked-out-item.png)\) for the checked out item beside a catalog item indicates that it's the published version of the item that has been checked out for editing in the catalog builder.
            -   A draft item icon \(![Draft item icon.](../image/draft-item.png)\) for the draft item mark beside the item indicates that it's the draft version of the item that can be directly edited in ServiceNow AI Platform.
        2.  Open the published item that you want to edit.
        3.  Select the **Edit checked out item in advanced view** related link.

            **Note:**

            -   When a published item is checked out for editing, you can't edit the published version of the item in ServiceNow AI Platform, unless you cancel the checkout in ServiceNow AI Platform. Canceling the checkout cancels all changes made after the item was checked out.
            -   To edit an item in the **In review** state, you must cancel the review. After you cancel the review, the state of the item is reverted to **Draft**.
2.  Make the required changes and select **Update**.

3.  To edit the same item in the catalog builder, select **Edit in Catalog Builder**.

    If the item has not already been checked out, this step checks out the item.


**Parent Topic:**[Edit a catalog item in Catalog Builder](edit-cat-item-cat-builder.md)

