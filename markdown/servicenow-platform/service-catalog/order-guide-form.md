---
title: Order guide form
description: Description of the fields on the Order guide form.
locale: en-US
release: xanadu
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Order guide form

Description of the fields on the Order guide form.

<table id="table_oqx_shn_cr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Order guide name that appears in the catalog.

</td></tr><tr><td>

Active

</td><td>

Check box to indicate whether the order guide is active or not.

</td></tr><tr><td>

Category

</td><td>

Category heading under which the order guide appears in the catalog.

</td></tr><tr><td>

Two step

</td><td>

Check box to enable two step ordering instead of the default [three-step ordering](../task/t_OrderProcess.md#), omitting the final step. With two step ordering, selecting **Check out** submits the request immediately, then displays the order confirmation screen. This is not applicable for Service Portal.

</td></tr><tr><td>

Icon

</td><td>

A 16x16 pixel image to appear as an icon beside the order guide name in the catalog. If no image is uploaded, the default icon appears beside this order guide.To use your own default icon, upload an image, overwriting the image stored in images/service\_catalog/generic\_small.gif.

</td></tr><tr><td>

Cascade variables

</td><td>

Check box to select whether the variables used cascade, which passes their values to the ordered items. If this check box is cleared, variable information entered in the order guide is not passed on to ordered items.

</td></tr><tr><td>

Ordered Item Link

</td><td>

Link to more information about an ordered item. Select a predefined link item to appear on the ordered item screen. Customers can click the link to access more information. This is not applicable for Service Portal.

</td></tr><tr><td>

Roles

</td><td>

Roles that users must have to access this order guide.

</td></tr><tr><td>

Short description

</td><td>

Summary of the order guide purpose.

</td></tr><tr><td>

Description

</td><td>

Description that appears on the first page of the order guide. Apply formatting with the HTML editor.

</td></tr><tr><td>

Meta

</td><td>

Comma-separated list of tags used to search for the order guide. See [Configure keyword search for catalog items](../task/search-catalog-item.md).

</td></tr><tr><td>

Hide on Service Portal

</td><td>

If selected, the order guide is not available on Service Portal.

</td></tr><tr><td>

Picture

</td><td>

\[Optional\] Image of the item.

</td></tr><tr><td>

Order to cart

</td><td>

Check box allowing users to add order guides to their cart, then continue shopping rather than checking out immediately. This is not applicable for Service Portal.**Note:** This setting only works when the Two step check box is also set to true.

</td></tr><tr><td class="sub-head" colspan="2">

Portal Settings

</td></tr><tr><td colspan="2">

Use these settings to configure the order guide behavior in Service Portal.

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

If selected, the **Add to Cart** button is not displayed for the order guide. If the **Show Add to Cart** instance option of the widget is set to false, then this setting is ignored.This setting is selected by default if the **Request method** is **Request** or **Submit**.

 For upgrade scenarios, if the **No cart** field is selected in Platform, run the CatalogPortalSettingsMigration script include to update this setting to the **Hide 'Add to Cart'** field in the **Portal Settings** tab.

</td></tr><tr><td>

Show Include Toggle

</td><td>

If selected, a toggle is displayed for each catalog item in the **Choose Options** section in Service Portal. You can click this toggle to include or exclude the catalog item from the order guide request.For zBoot customers, this option is selected by default for existing order guides in the demo data and new order guides.

 For upgrade customers, this option is selected by default only for new order guides.

</td></tr></tbody>
</table>For information about creating an order guide, see [Create an order guide](../task/t_CreateAnOrderGuide.md).

**Parent Topic:**[Service Catalog Reference](../concept/service-catalog-reference.md)

