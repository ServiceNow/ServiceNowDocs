---
title: Create or edit a catalog item
description: Define individual catalog items using Service Catalog. You can create, edit, and copy catalog items.Catalog administrators can edit an item from the service catalog listing. Catalog managers and catalog editors can also edit an item if they are assigned to the item.Copy an item to create a full duplicate of the item, including the item details, attachments, variables, client scripts, and approvals.Accessibility checker in the toolbar enables you to identify and resolve accessibility related issues while creating a catalog item in Service Catalog.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Types of catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create or edit a catalog item

Define individual catalog items using Service Catalog. You can create, edit, and copy catalog items.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definition** &gt; **Maintain Items**.

2.  Click **New**.

3.  On the Catalog Item form, fill in the fields.

    For more information about the fields and their descriptions on the Catalog Item form, see [Catalog Item form](../reference/catalog-item-form.md).

4.  Click **Submit**.


## What to do next

-   Assign the item to additional catalogs and categories, if required.
-   Define [variables](../concept/c_ServiceCatalogVariables.md) for the item, if applicable.
-   To add attachments such as information and instruction documentation to the catalog item, see [Add an attachment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/t_AddingAnAttachment.md).

Read related topics:

-   [Create a service catalog variable](t_CreateAVariableForACatalogItem.md)
-   [Apply user criteria to items](t_AppUserCritItemsCat.md#)
-   [Set a recurring price](../concept/c_SetARecurringPrice.md)

**Parent Topic:**[Types of catalog items](../reference/r_ExtendedCatalogItemFunctions.md)

## Edit a catalog item

Catalog administrators can edit an item from the service catalog listing. Catalog managers and catalog editors can also edit an item if they are assigned to the item.

### Before you begin

Role required: admin

### About this task

To edit a catalog item from the service catalog listing:

### Procedure

1.  Right-click the header and select one of the following options:

    -   **Configure Variables**: Add or remove variables from an item.
    -   **New Variable**: Create a new variable for the item.
    -   **Configure Item**: Edit the item definition.
    -   **Configure Client Scripts**: Edit the catalog client scripts for the item.
    -   **Configure UI Policies**: Edit the catalog UI policies for the item.

## Copy a catalog item

Copy an item to create a full duplicate of the item, including the item details, attachments, variables, client scripts, and approvals.

### Before you begin

Role required: admin

### About this task

Copying can be more useful than using the Insert function because the function only copies the item details.

### Procedure

1.  Open a catalog item form.

2.  Use the **Copy** button to create a new copy of a catalog item, named **Copy of \[item name\]**.

    **Note:**

    -   If you copy an active catalog item, the copy is also active. Consider deactivating the copy by clearing the **Active** check box until your changes are complete.
    -   When you specify a table in the **Relationship tables which should be part of the Copy Item Action. Table names should be comma separated** property in the **Service Catalog** &gt; **Catalog Administration** &gt; **Properties** page, the table records that have a reference to a catalog item are also copied. It is applicable only when you copy the catalog item using the **Copy** UI action. Table names should be comma-separated without any spaces.

## Accessibility checker in the toolbar

Accessibility checker in the toolbar enables you to identify and resolve accessibility related issues while creating a catalog item in Service Catalog.

### Before you begin

Role required: admin

Confirm that the following properties contain the correct values for accessibility checker:

|Property|Value|
|--------|-----|
|glide.ui.html.editor.toolbar|a11ycheck|
|glide.ui.html.editor.enabled\_plugins|a11ychecker|

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definition** &gt; **Maintain Items**.

2.  Select **New**.

    **Note:** If you want to check the accessibility of the content for an existing catalog item, select the catalog item form the list.

3.  Select the Item Details tab.

4.  In the **Description** field, select the accessibility checker icon ![accessibility checker icon](../../knowledge-management/image/accessibility-checker-icon.png) in the toolbar.

5.  View accessibility-related issues in the **Accessibility Checker** window along with suggestions for resolution of each issue.

6.  Select **Repair** to implement the suggestion, or **Ignore**.

    If there are no accessibility issues in the article, then the **Accessibility Checker** window displays a success message:

    No accessibility issues detected


