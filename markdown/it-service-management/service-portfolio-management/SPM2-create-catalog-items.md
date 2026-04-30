---
title: Create catalog items for service offering subscribers in Service Portfolio Management
description: As a service owner or service offering subscriber, you can create one or more catalog items for your service regardless of the offering phase or status. You can also relate an existing catalog item to a service offering.
locale: en-US
release: yokohama
product: Service Portfolio Management
classification: service-portfolio-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Service offerings in Service Portfolio Management, Using Service Portfolio Management, Service Portfolio Management, IT Service Management]
---

# Create catalog items for service offering subscribers in Service Portfolio Management

As a service owner or service offering subscriber, you can create one or more catalog items for your service regardless of the offering phase or status. You can also relate an existing catalog item to a service offering.

## Before you begin

Role required: com.snc.service\_portfolio or service\_editor

## About this task

Use the **Items orderable by subscribers** related list \(tab\) on a service offering to:

-   Relate an existing catalog item to a service offering.
-   Create catalog items for a service offering.

## Procedure

1.  Navigate to **All** &gt; **Service Portfolio Management** &gt; **Service offerings**.

2.  Open a service offering that you want to relate a catalog item to or add a catalog item to.

3.  Select the **Items orderable by subscribers** tab.

4.  Relate a catalog item to an existing service offering.

    1.  Select **Edit** to see a list of catalog items that you can relate to the service offering. The list of catalog items includes record producers. To see a list of record producers, open a new tab and type **sc\_cat\_item\_producer.list** in the Filter navigation field.
    2.  Move the catalog item from the **Collection** list to the **Items orderable by subscribers List**.
    3.  After you have moved all the catalog items that you want to relate to the service offering, select **Save**.
5.  Create a catalog item for the service offering.

    1.  Select **New**.
    2.  On the form, fill in the fields.

<table id="table_cgz_rcm_wxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the catalog item.

</td></tr><tr><td>

Catalogs

</td><td>

The catalogs that this item is related with.

</td></tr><tr><td>

Category

</td><td>

Category for the item. Adding the catalog enables others to search for this item.

</td></tr><tr><td>

State

</td><td>

State of the catalog item. When creating a catalog item, you can't edit the **State** field. The state changes to **Draft** after you select **Submit**.

</td></tr><tr><td>

Checked out

</td><td>

Name of the person who has the catalog item checked out for editing.

</td></tr><tr><td>

Owner

</td><td>

Owner of the catalog item.

</td></tr><tr><td>

Fulfillment automation level

</td><td>

The fulfillment level of the catalog item.

</td></tr><tr><td class="sub-head" colspan="2">

Item Details

</td></tr><tr><td>

Short Description

</td><td>

Short description that is viewed on the service catalog homepage, search results, and the title bar of the order form.

</td></tr><tr><td>

Description

</td><td>

Full description of the catalog item. You can embed videos, images, links to internal Knowledge Base \(KB\) articles, and links to external sources of information.

</td></tr><tr><td>

Meta

</td><td>

Comma-separated list of tags used to search for the catalog item. Use commas between keywords for better results when searching.

 For more information, see [Configure keyword search for catalog items](https://www.servicenow.com/docs/access?context=search-catalog-item&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td class="sub-head" colspan="2">

Process Engine**Note:** You can specify a value for only one of these fields.

</td></tr><tr><td>

Flow

</td><td>

Flow that defines the fulfillment of the catalog item.

</td></tr><tr><td>

Workflow

</td><td>

Workflow that defines the fulfillment of the catalog item.

</td></tr><tr><td>

Execution plan

</td><td>

Execution plan that defines the delivery of the catalog item.

</td></tr><tr><td class="sub-head" colspan="2">

Picture

</td></tr><tr><td>

Icon

</td><td>

Image next to the catalog item in the catalog. The icon dimensions are 27x27 pixels. If no image is uploaded, the default icon is next to the catalog item. Your uploaded image overwrites the default image stored in `images/service_catalog/generic_small.gif`.

</td></tr><tr><td>

Picture

</td><td>

Image of the item.

</td></tr><tr><td class="sub-head" colspan="2">

Pricing

</td></tr><tr><td>

Price

</td><td>

Price for the catalog item. Select the currency from the list.

</td></tr><tr><td>

Recurring Price

</td><td>

Price for the catalog item that recurs. For example, a maintenance service could have a monthly recurring price.

</td></tr><tr><td>

Recurring Price Frequency

</td><td>

Time frame for recurrence, such as **Monthly** or **Annually**.

</td></tr><tr><td class="sub-head" colspan="2">

Portal Settings

</td></tr><tr><td colspan="2">

Use these settings to configure the catalog item behavior in the Service Portal.

</td></tr><tr><td>

Request method

</td><td>

Setting that controls the label for the **Order Now** button and the order submission experience. -   **Order**:

    -   Button label: **Order Now**
    -   Confirmation dialog box: Displayed
    -   Delivery information: Editable
**Note:** This setting is the default setting.

-   **Request**:

    -   Button label: **Request**
    -   Confirmation dialog box: Displayed
    -   Delivery information: Not displayed
This setting can be used in scenarios such as a code access request where the delivery information is pre-determined.

-   **Submit**:

    -   Button label: **Submit**
    -   Confirmation dialog box: Not displayed
    -   Delivery information: Not displayed
This setting can be used in scenarios such as a reset password request where no further request information is required.

</td></tr><tr><td>

Hide 'Add to Cart'

</td><td>

If selected, the **Add to Cart** button isn’t displayed for the item. If the **Show Add to Cart** instance option of the widget is set to **false**, then this setting is ignored.This setting is selected by default if the **Request method** is **Request** or **Submit**.

 For upgrade scenarios, if the **No cart** field is selected in Platform, then run the CatalogPortalSettingsMigration script include to update this setting to the **Hide 'Add to Cart'** field on the **Portal Settings** tab.

 **Note:** This field is applicable for a catalog item and order guide.

</td></tr><tr><td>

Hide Quantity

</td><td>

If selected, the **Quantity** list isn’t displayed for the catalog item. **Hide Quantity** is selected by default if the **Request method** is **Request** or **Submit**.

 For upgrade customers, if the **No quantity** field is selected in Platform, run the CatalogPortalSettingsMigration migration script to update this setting to the **Hide Quantity** field on the **Portal Settings** tab.

 **Note:**

-   Applicable for a catalog item.
-   An order guide inherits this setting from the included catalog item.


</td></tr><tr><td>

Hide Delivery time

</td><td>

If selected, the **Delivery Time** field isn’t displayed for the catalog item.**Hide Delivery time** is selected by default if the **Request method** is **Submit**.

 **Note:**

-   Applicable for a catalog item.
-   An order guide inherits this setting from the included catalog item.


</td></tr><tr><td>

Hide 'Add to Wish List'

</td><td>

If selected, the **Add to wish list** button isn’t displayed for the catalog item. If the wish list is inactive for the catalog item or the portal widget instance option is set to **false**, then this setting is overridden for the item. **Note:** Applicable for a catalog item and record producer.

</td></tr><tr><td>

Hide Attachment

</td><td>

If selected, the **Add attachments** button isn’t displayed for the catalog item.**Note:**

-   Applicable for a catalog item and record producer.
-   An order guide inherits this setting from the included catalog item.


</td></tr><tr><td>

Mandatory Attachment

</td><td>

If selected, adding an attachment is required for the catalog item.**Note:** Applicable for a catalog item and record producer.

</td></tr></tbody>
</table>6.  **Submit**.

    Before you submit, select **Try It** to see the result.


**Parent Topic:**[Service offerings in Service Portfolio Management](../concept/SPM2-service-offerings.md)

