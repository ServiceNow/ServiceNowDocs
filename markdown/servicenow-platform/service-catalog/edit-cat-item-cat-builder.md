---
title: Edit a catalog item in Catalog Builder
description: Make changes to an existing catalog item if you have permissions to edit the item.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Creating or editing catalog item template, Catalog Builder, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Edit a catalog item in Catalog Builder

Make changes to an existing catalog item if you have permissions to edit the item.

## Before you begin

-   You can edit a catalog item if you are a catalog admin.
-   If you have the catalog\_builder\_editor role and you are the owner of the catalog item, you can edit it. If the template access property, **glide.sc.builder.template\_access**, is set to **true** \(which is **false** by default\), any user with the catalog\_builder\_editor role with access to the template used for creating the catalog item can edit the item.
-   Role required: catalog\_builder\_editor, catalog\_admin, or admin

## About this task

When you edit a published item in the catalog builder, the system creates a draft copy of the item and its associated records such as variables, UI policies, and client scripts. The draft version is inactive until published. The published item remains in the published state and the **Checked out** field is set to **True**.

After you edit the item and submit it, the following scenarios are possible:

-   **When a pre-publish subflow isn't configured**
    -   The edits to the draft version are merged with the associated published item.
    -   The draft item and the associated records are deleted.
    -   The **Checked out** field of the published item is set to **False**.
-   **When a pre-publish subflow is configured**
    -   The state of the draft item is changed to **In review**.
    -   If the **state** variable of the subflow output returns **Completed**:
        -   The state of the draft item is changed to **Reviewed** and edits made to the draft version are merged with the associated published item.
        -   The state of the published item changes to **Publishing**, then to **Published**, and the **Checked out** field of the published item is set to **False**. The state change from **Publishing** to **Published** may not happen instantaneously.
        -   The reviewed draft item and the associated records are deleted.
    -   If the **state** variable of the subflow output returns **Failed**, the state of the draft item is reverted to **Draft**, and the item is ready for editing.

For information about configuring a review subflow, see [Setting up the Catalog Builder](set-up-cat-builder.md).

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Builder**.

2.  Select the **Catalog items** tab.

    **Note:** In the catalog item list view of the catalog builder, you can view items based on the value set in the **glide.sc.builder.item\_filter\_mode** property.

3.  Select the item that you want to edit and select **Edit**.

    **Note:**

    -   To edit an item in the **In review** state, you must cancel the review. After you cancel the review, the state of the item is reverted to **Draft**.
    -   To view the conversational details of the catalog item, select **View conversational details**.
    To edit an item in the **In review** state, you must cancel the review. After you cancel the review, the state of the item is reverted to **Draft**.

4.  Make the required changes and select **Save**.

    For information on editing a question and catalog item fields, see [Edit a question in Catalog Builder](edit-question-cat-builder.md) and [Create a catalog item using a template](create-item-cat-builder.md).

5.  To make an item inactive, clear the **Item is active** check box in the **Basic info** section of the **Details** step.

6.  To publish the modified item, navigate to the **Review and submit** step and select **Submit**.


-   **[Add advanced capabilities to a catalog item](add-advanced-capabilities.md)**  
Add advanced capabilities, such as catalog client scripts, data lookup rules, and advanced reference qualifiers to a catalog item.
-   **[Discard a catalog item](discard-a-catalog-item.md)**  
Discard a catalog item that’s in the Draft state in Catalog Builder.

**Parent Topic:**[Creating or editing catalog item template](create-cat-item-template-cat-builder.md)

**Related topics**  


[View the conversational catalog overview dashboard using Catalog Builder](view-conversational-dashboard.md)

