---
title: Operational Technology Catalog Item form
description: When creating a new catalog item for the Operational Technology \(OT\) Service Catalog, fill out the following form fields.
locale: en-US
release: xanadu
product: Operational Technology Request Management
classification: operational-technology-request-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Reference, Operational Technology Request Management, Operational Technology]
---

# Operational Technology Catalog Item form

When creating a new catalog item for the Operational Technology \(OT\) Service Catalog, fill out the following form fields.

The following tables describe the fields available in each section of the OT Catalog Item form.

<table id="table_zvc_txl_3bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Basic Info

</td></tr><tr><td>

Item name

</td><td>

Name to appear in the catalog.

</td></tr><tr><td>

Short description

</td><td>

Text that appears on the service catalog homepage, search results, and the title bar of the order form.

</td></tr><tr><td colspan="2">

Item details

</td></tr><tr><td>

Image

</td><td>

Image of the item.

</td></tr><tr><td>

Description

</td><td>

Full description of the item. This description appears in the catalog when a user selects the item or clicks the associated **Preview** link.

 You can embed videos, images, links to internal knowledge base \(KB\) articles, and links to external sources of information and instruction documentation.

</td></tr></tbody>
</table><table id="table_acx_5xl_3bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Catalogs

</td></tr><tr><td>

Selected catalogs

</td><td>

Catalogs this item appears in.

</td></tr><tr><td colspan="2">

Categories

</td></tr><tr><td>

Selected categories

</td><td>

Category for the item. Categories can only be selected after the **Catalogs** field is populated.

 Catalog searches find only items assigned to a category in the Service Portal.

</td></tr><tr><td colspan="2">

Topics

</td></tr><tr><td>

Selected topics

</td><td>

Topics for the item. Requesters can use the topics you added to find and access the catalog item once the catalog item is published.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|OT Catalog Item Variable Set|
|Site|Site that’s affected by the catalog item.|

<table id="table_fnb_dyl_3bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Portal settings

</td></tr><tr><td>

Submit button label

</td><td>

Label for the submit button after the requester finishes filling out the catalog item form.

</td></tr><tr><td>

Hide 'Add to cart' button

</td><td>

If selected, the **Add to Cart** button is not displayed for the item. If the **Show Add to Cart** instance option of the widget is set to false, then this setting is ignored. This setting is selected by default if the **Request method** is **Request** or **Submit**.

For upgrade scenarios, if the **No cart** field is selected in Platform, run the `CatalogPortalSettingsMigration` script include to update this setting to the **Hide 'Add to Cart'** field in the **Portal Settings** tab.

**Note:** Applicable for a catalog item and order guide.

</td></tr><tr><td>

Hide ‘Save as draft’ button

</td><td>

If selected, the **Save as draft** button is not displayed for the item.

</td></tr><tr><td>

Hide quantity selector

</td><td>

If selected, the **Quantity** list is not displayed for the catalog item. This is selected by default if the **Request method** is **Request** or **Submit**.

For upgrade customers, if the **No quantity** field is selected in Platform, run the `CatalogPortalSettingsMigration` migration script to update this setting to the**Hide Quantity** field in the **Portal Settings** tab.

**Note:** Applicable for a catalog item.

An order guide inherits this setting from the included catalog item.

</td></tr><tr><td>

Hide delivery time

</td><td>

If selected, the **Delivery Time** field is not displayed for the catalog item.

 This is selected by default if the **Request method** is **Submit**.

 **Note:** Applicable for a catalog item.

 An order guide inherits this setting from the included catalog item.

</td></tr><tr><td>

Hide attachment button

</td><td>

If selected, the **Add attachments** button is not displayed for the catalog item.

**Note:** Applicable for a catalog item and record producer.

 An order guide inherits this setting from the included catalog item.

</td></tr><tr><td>

Make attachment mandatory

</td><td>

If selected, adding an attachment is mandatory for the catalog item.

**Note:** Applicable for a catalog item and record producer.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Available for|
|User criteria granted access|Select the user criteria that can access the catalog item.|
|Not available for|
|User criteria denied access|Select the user criteria that cannot access the catalog item.|

<table id="table_cyz_jzl_3bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Fulfillment method

</td></tr><tr><td>

Process engine

</td><td>

Sequence for item request fulfillment.

</td></tr><tr><td>

Selected flow

</td><td>

Flow that defines how the item request is fulfilled. **Note:** This field is only visible if you select **Flow Designer Flow** in the **Process engine** field.

</td></tr><tr><td>

Selected workflow

</td><td>

Workflow that defines how the item request is fulfilled.

**Note:** This field is only visible if you select **Workflow** in the **Process engine** field.

</td></tr></tbody>
</table>**Parent Topic:**[Operational Technology Request Management reference](../concept/operational-technology-request-management-reference.md)

