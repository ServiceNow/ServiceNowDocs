---
title: Catalog Item form
description: Description of the fields on the Catalog Item form.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 12
breadcrumb: [Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Catalog Item form

Description of the fields on the Catalog Item form.

<table id="table_vhv_ywr_bq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to appear in the catalog.

</td></tr><tr><td>

Catalogs

</td><td>

Catalogs this item appears in.

</td></tr><tr><td>

Category

</td><td>

Category for the item. Categories can only be selected after the **Catalogs** field is populated.Catalog searches find only items that are assigned to a category in the Service Portal.

 For Employee Center, catalog searches find only items that are associated with a taxonomy topic. For more information, see [Associate a catalog item with a taxonomy topic in Employee Center](../task/associate-cat-item-taxonomy-ec.md).

</td></tr><tr><td>

Model

</td><td>

Product model to which the item is linked. This field is visible by default only for items created by publishing models.Click the reference icon to view the product model.

</td></tr><tr><td>

Active

</td><td>

Check box to make the item active \(available to be ordered\).**Note:** Inactive catalog items added to order guides do not appear in the order guide. Use **Visible On Guide**, **Visible elsewhere** to hide the item and show only in the order guide.

</td></tr><tr><td>

Fulfillment automation level

</td><td>

Option to specify the level of fulfillment automation for catalog item requests. The available options are:-   Unspecified: Automation level of catalog item is not specified.
-   Manual: Catalog item is not automated.
-   Semi-automated: Catalog item is semi-automated.
-   Fully automated: Catalog item is completely automated.

</td></tr><tr><td>

Access Type

</td><td>

Option to specify if a request can be submitted for a user who does not have access to the catalog item. Possible options are:-   Restricted: The request can only be submitted for users who have access to the catalog item.
-   Delegated: The request can be submitted even for users who do not have access to the catalog item.

 By default, this field is set to `Restricted`. For information about delegated request experience, see [Delegated request experience](../concept/delegated-request-exp.md).

 **Note:** This functionality is only applicable when the catalog item has a Requested For variable.

</td></tr><tr><td>

Owner

</td><td>

Owner of the catalog item who has edit access to it​.

</td></tr><tr><td>

Template

</td><td>

Template using which the item is created.

</td></tr><tr><td>

Preview Link

</td><td>

Click **Preview Item** to preview in a new window how the current item definition would look in the catalog.

</td></tr><tr><td>

Ordered Item Link

</td><td>

Link to preview, as shown on the ordered item screen.

</td></tr><tr><td>

Hide on Service Portal

</td><td>

If selected, the catalog item is not available on Service Portal.

</td></tr><tr><td>

Availability

</td><td>

Devices to display the item: **Desktop and Classic Mobile**, **Desktop Only**, or **Classic Mobile Only**.**Note:** Unsupported catalog item types are not displayed on Classic Mobile devices, even if **Availability** is set to show an item of this type.

</td></tr><tr><td class="sub-head" colspan="2">

Item Details

</td></tr><tr><td>

Short Description

</td><td>

Text that appears on the service catalog homepage, search results, and the title bar of the order form.

</td></tr><tr><td>

Description

</td><td>

Full description of the item. This description appears in the catalog when a user selects the item or clicks the associated **Preview** link.You can embed videos, images, links to internal knowledge base \(KB\) articles, and links to external sources of information and instruction documentation.

</td></tr><tr><td>

Meta

</td><td>

Comma-separated list of tags used to search for the catalog item. Use commas between keywords for better results when searching. The Zing search engine removes common words from search queries that do not produce meaningful results.See [Configure keyword search for catalog items](../task/search-catalog-item.md).

</td></tr><tr><td class="sub-head" colspan="2">

Process Engine**Note:** You can specify a value for only one of these fields.

</td></tr><tr><td>

Flow

</td><td>

Flow that defines how the item request is fulfilled.

</td></tr><tr><td>

Workflow

</td><td>

Workflow that defines how the item request is fulfilled.

</td></tr><tr><td>

Execution plan

</td><td>

Execution plan \(formerly named delivery plan\) that defines how the item request is fulfilled.

</td></tr><tr><td class="sub-head" colspan="2">

Picture

</td></tr><tr><td>

Icon

</td><td>

Image to appear as an icon beside the item name in the catalog. Upload a 27x27 pixel image. If no image is uploaded, the default icon appears beside this item. To use your own default icon, upload an image. The uploaded image overwrites the default image stored in `images/service_catalog/generic_small.gif`.

</td></tr><tr><td>

Picture

</td><td>

Image of the item.

</td></tr><tr><td class="sub-head" colspan="2">

Classic Mobile

</td></tr><tr><td>

Classic Mobile Picture Type

</td><td>

Type of picture to display for the item on mobile devices. Set to **Desktop** to use the standard desktop picture, **Classic Mobile** to use a specific image for the mobile device using the **Mobile picture** field, or **None** to not use a picture.

</td></tr><tr><td>

Classic Mobile Picture

</td><td>

Image file for the mobile picture. The field appears if **Classic Mobile picture type** is set to **Classic Mobile**.

</td></tr><tr><td>

Hide Price \(classic mobile listings\)

</td><td>

Check box to hide the item price on mobile devices. Clear the check box to display the price.

</td></tr><tr><td class="sub-head" colspan="2">

Pricing

</td></tr><tr><td>

Price

</td><td>

Price for the item. Select the currency from the choice list.

</td></tr><tr><td>

Recurring Price

</td><td>

Price that occurs repeatedly at a regular interval. For example, a printer maintenance service could have a $100.00 monthly recurring price.

</td></tr><tr><td>

Recurring Price Frequency

</td><td>

Time frame for recurrence, such as **Monthly** or **Annually**, only if the **Recurring Price** field has an entry.

</td></tr><tr><td>

Omit Price in Cart

</td><td>

Check box to hide the item price in the cart and the catalog listing.

</td></tr><tr><td class="sub-head" colspan="2">

Portal Settings

</td></tr><tr><td colspan="2">

Use these settings to configure the catalog item behavior in Service Portal.

</td></tr><tr><td>

Request method

</td><td>

Setting that controls the label displayed for the **Order Now** button and the order submission experience. -   **Order**:

    -   Button label: **Order Now**
    -   Confirmation dialog box: Displayed
    -   Delivery information: Editable
**Note:** This is the default setting.

-   **Request**:

    -   Button label: **Request**
    -   Confirmation dialog box: Displayed
    -   Delivery information: Not displayed.
This setting can be used in scenarios such as a code access request where the delivery information is pre-determined.

-   **Submit**:

    -   Button label: **Submit**
    -   Confirmation dialog box: Not displayed
    -   Delivery information: Not displayed
This setting can be used in scenarios such as reset password request where no further request information is required.


</td></tr><tr><td>

Hide 'Add to Cart'

</td><td>

If selected, the **Add to Cart** button is not displayed for the item. If the **Show Add to Cart** instance option of the widget is set to false, then this setting is ignored.This setting is selected by default if the **Request method** is **Request** or **Submit**.

 For upgrade scenarios, if the **No cart** field is selected in Platform, run the CatalogPortalSettingsMigration script include to update this setting to the **Hide 'Add to Cart'** field in the **Portal Settings** tab.

 **Note:** Applicable for a catalog item and order guide.

</td></tr><tr><td>

Hide 'Save as draft'

</td><td>

If selected, the **Save as Draft** button isn't displayed for the item on the portals.

 You can let requesters save a draft of a catalog item while requesting it on the portals such as Employee Center and Service Portal, and Now Mobile app. The requesters can access the saved drafts from the My Request widget in the **Drafts** tab on the portals and edit the drafts.

</td></tr><tr><td>

Hide Quantity

</td><td>

If selected, the **Quantity** list is not displayed for the catalog item. This is selected by default if the **Request method** is **Request** or **Submit**.

 For upgrade customers, if the **No quantity** field is selected in Platform, run the CatalogPortalSettingsMigration migration script to update this setting to the **Hide Quantity** field in the **Portal Settings** tab.

 **Note:**

-   Applicable for a catalog item.
-   An order guide inherits this setting from the included catalog item.

</td></tr><tr><td>

Hide Delivery time

</td><td>

If selected, the **Delivery Time** field is not displayed for the catalog item.This is selected by default if the **Request method** is **Submit**.

 **Note:**

-   Applicable for a catalog item.
-   An order guide inherits this setting from the included catalog item.

</td></tr><tr><td>

Hide 'Add to Wish List'

</td><td>

If selected, the **Add to wish list** button is not displayed for the catalog item. If the wish list is disabled for the catalog item or the portal widget instance option is set to false, then this setting is overridden for the item. **Note:** Applicable for a catalog item and record producer.

</td></tr><tr><td>

Hide Attachment

</td><td>

If selected, the **Add attachments** button is not displayed for the catalog item.**Note:**

-   Applicable for a catalog item and record producer.
-   An order guide inherits this setting from the included catalog item.

</td></tr><tr><td>

Mandatory Attachment

</td><td>

If selected, adding an attachment is mandatory for the catalog item.**Note:** Applicable for a catalog item and record producer.

</td></tr><tr><td class="sub-head" colspan="2">

Universal Request Config

</td></tr><tr><td colspan="2">

This section is available only when the Universal Request plugin \(com.snc.universal\_request\) is activated. For information about this configuration, see [Service Catalog configuration for Universal Request](../concept/ur-catalog-config.md).

</td></tr><tr><td>

UR certified/enabled item

</td><td>

Option to specify that a universal request should also be created along with a requested item. In the universal request, a reference is created to the associated requested item, which becomes the primary task of the universal request.

</td></tr><tr><td>

Requires Additional Review

</td><td>

Option to automatically select the **Needs resolution review** check box on the corresponding universal request. For information about the universal request fields, see [Universal Request form](https://www.servicenow.com/docs/access?context=new-ur-record-form&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US).The **Requires Additional Review** field appears only when the **UR certified/enabled item** check box is selected.

</td></tr><tr><td class="sub-head" colspan="2">

Fields that can be added by configuring the form

</td></tr><tr><td>

Expand help for all questions

</td><td>

Check box to expand and display [help information](../task/t_DefineHelpInformation.md) for all questions on loading the page.**Note:**

-   This field is also applicable in Service Portal.
-   If the **Expand help for all questions** check box is selected at the catalog item level, then the **Always Expanded** field setting at the variable level is overridden.
-   If the **Expand help for all questions** check box is deselected at the catalog item level, then the **Always Expanded** field setting at the variable level is applicable.

</td></tr><tr><td>

Template

</td><td>

Template to populate the generated record with predefined values. The field is available for **Record Producer** items only.

</td></tr><tr><td>

No Quantity

</td><td>

Check box to hide the quantity selector for the item.

</td></tr><tr><td>

No Cart

</td><td>

Check box to hide the shopping cart for the item.

</td></tr><tr><td>

No search

</td><td>

Check box to prevent this item from being listed in search results and also in the Service Catalog widget on the Service Portal.If this is selected:

-   In Service Portal, you can neither browse nor search for the item.
-   In Platform, you can browse to find the item.

</td></tr><tr><td>

Order

</td><td>

Controls the ordering of items in category lists.

</td></tr><tr><td>

Domain

</td><td>

Domain in which the catalog item is created. Applicable when the domain separation is enabled in Service Catalog. For information about domain separation, see [Domain separation and Service Catalog](../concept/domain-separation-service-catalog-management.md).

</td></tr><tr><td>

Domain Path

</td><td>

Series of three-character codes separated by a slash \(/\) delimiter to identify a domain. This path string is unique in the domain hierarchy. Applicable when the domain separation is enabled in Service Catalog.

</td></tr><tr><td class="sub-head" colspan="2">

**Related Links**

</td></tr><tr><td>

Item Diagnostic

</td><td>

Generates a [diagnostic](../concept/c_ItemDiagnostic.md) report and score to identify possible issues within the Service Catalog data and configuration.

</td></tr><tr><td>

Edit checked out item in advanced view

</td><td>

Allows you to edit the catalog item in the advanced view. To add a catalog client script to a checked out item in the Draft state, you can click this related link and add the catalog client script using the Catalog Client Scripts related list.**Note:** This option is available only after you click **Edit in Catalog Builder** to edit an item in catalog builder.

</td></tr><tr><td class="sub-head" colspan="2">

**Related Lists**

</td></tr><tr><td>

Variables

</td><td>

[Variables](../task/t_CreateAVariableForACatalogItem.md) for the item to provide options for ordering the item.

</td></tr><tr><td>

Variable Sets

</td><td>

[Variable Set](../concept/c_ServiceCatalogVariableSets.md) linked to the item.Link an existing variable set to the item to provide multiple options for ordering the item.

</td></tr><tr><td>

Approved By Group

</td><td>

Groups that must approve requests for this item.

</td></tr><tr><td>

Approved By

</td><td>

Users who must approve requests for this item.

</td></tr><tr><td>

Categories

</td><td>

Additional [categories](../task/t_CreateACategory.md) associated with this item.

</td></tr><tr><td>

Catalogs

</td><td>

Additional [catalogs](../concept/c_MultipleServiceCatalogs.md#) associated with this item.

</td></tr><tr><td>

Catalog Data Lookup Definitions

</td><td>

Catalog data lookup rules associated with the catalog item. For information on creating a data lookup rule, see [Create a catalog lookup definition](../task/t_CreatACatDataLookupDefRec.md#).

</td></tr><tr><td>

Catalog UI Policies

</td><td>

[Catalog UI policies](../concept/c_ServiceCatalogUIPolicy.md) associated with this item.

</td></tr><tr><td>

Catalog Client Scripts

</td><td>

[Catalog client scripts](../task/t_CreateACatalogClientScript.md) associated with this item.

</td></tr><tr><td>

Related Items

</td><td>

Related items for a catalog item to provide alternatives. These items are displayed in the catalog item page in Service Portal and Now Mobile.

</td></tr><tr><td>

Related Articles

</td><td>

Related articles for a catalog item to provide additional information. These articles are displayed in the catalog item page in Service Portal and Now Mobile.

</td></tr><tr><td>

Service Fulfillment Steps

</td><td>

Associated service fulfillment steps.

</td></tr><tr><td>

Assigned Topics

</td><td>

Associate a catalog item to a taxonomy and topic. For information about how to add an item to a taxonomy, see [Associate a catalog item with a taxonomy topic in Employee Center](../task/associate-cat-item-taxonomy-ec.md).**Note:** This field becomes available when you activate the Employee Experience Taxonomy plugin \(sn\_ect\).

</td></tr></tbody>
</table>For information about creating or editing a catalog item, see [Create or edit a catalog item](../task/t_DefineACatalogItem.md#).

**Parent Topic:**[Service Catalog Reference](../concept/service-catalog-reference.md)

