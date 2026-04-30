---
title: Create multiple configurations
description: Create multiple configurations of a child product offering when you're adding a configurable product to an opportunity, quote, or order. You can then configure the product options and characteristics separately for each offering configuration.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Legacy product configurator, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Create multiple configurations

Create multiple configurations of a child product offering when you're adding a configurable product to an opportunity, quote, or order. You can then configure the product options and characteristics separately for each offering configuration.

## Before you begin

Role required:sales\_agent or sn\_ind\_tmt\_orm.order\_agent

## About this task

If your product catalog admin has enabled multiple configurations for child offerings in a bundled product, you can create multiple child offering configurations for selected child offerings using the legacy product configurator. When creating multiple configurations of child offering, you can do the following:

-   Change the quantity of a child offering that can have multiple configurations.
-   Clone a child offering or split a child offering that has a quantity greater than 1.
    -   The **Clone** option copies the child offering based on the number of copies that you specify and creates identical offering configurations.
    -   The **Split** option divides the current child offering quantity by the number of splits that you specify and distributes the quantity evenly across all the copies.
-   Customize the options and characteristics for each child offering instance created.
-   Delete a child offering instance, as long as the minimum number of child offerings defined for the product is maintained.

**Note:** Even when the multiple configurations feature is enabled, there are scenarios in which some configuration options might not be available. The system uses the default, minimum, and maximum quantity values from the product definition to determine valid configurations and then enables or disables the **Split** or **Delete** options for managing child offering configurations. For more information on validation, see [Multiple configurations](../concept/multiple-child-offering-configurations.md).

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../../../reuse/icons/product-icons/list-outline-24.svg) view.

2.  Navigate to the opportunity, quote, or order that you want to work with.

    For example, navigate to **Quotes** &gt; **All** and select the quote that you want to work with.

3.  Select the Catalog tab.

4.  In the product catalog hierarchy, select the product catalog that you want to use.

    The product catalog displays the available products as product offering cards.

5.  Select the configurable product by choosing **Customize** in the appropriate product offering card.

    The product configurator displays the product offering configuration, including the bundle product options and characteristics. Child offerings that can have multiple configurations are identified by Information icons. Select the Information icon to view a message indicating that the offering can have multiple configurations and that the offering quantity shown is aggregated across the configurations.

    ![Information message displayed for a child offering in a configurable product. The message indicates that multiple configurations can be created for the offering.](../image/multi-config-msg-order.png "Example bundle configuration for an order")

6.  Navigate to the child offering in the product hierarchy, which displays the offering summary page.

    You can do the following:

    -   To change the quantity of the child offering, enter the new value in the **Quantity** field.
    -   To add new configurations for the offering, select the **More options** ![](../image/icon-three-dots.png) \) menu next to the **Quantity** field and select an option.

<table id="table_nsy_k4f_kfc"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Clone

</td><td>

Option for creating copies of the selected child offering. Enter the number of clones to be created. The system creates identical copies of the child product offering, and each clone has a quantity of 1.For example, if the current child offering quantity is 2, and you specify 2 clones, two identical copies of the child offering are created. Each clone has a quantity of 1 and becomes a separate line item that you can configure.

**Note:** The system checks the total quantity allowed for the child offering.

</td></tr><tr><td>

Split

</td><td>

Option for creating child offering instances by splitting the current child offering quantity and distributing the quantities across the offering instances. Enter the number of splits to be used. For example, if the child offering quantity is 5, and you specify 3 splits, the system creates two child offering instances. After the split, you have three child offering instances, which have a quantity of 2, 2, and 1, respectively. You can then configure each line item as needed.

</td></tr><tr><td>

Delete

</td><td>

Removes an existing child offering instance.

</td></tr></tbody>
</table>    New configurations resulting from the clone or split are listed in the product catalog hierarchy. The associated pricing is displayed in the Current Selection pane.

    -   New configurations have names that reflect the child offering name, followed by an incremental number, for example, Home Automation Hub 2, Home Automation Hub 3, and so on.
    -   Quantity changes for a child offering are also reflected in the Current Selection pane.
7.  For each new offering configuration, select the appropriate characteristics and product options.

8.  When you finish configuring the child offerings, select **Add** to add each configuration as a separate line item to your opportunity, quote, or order.


**Parent Topic:**[Using the legacy product configurator](../concept/using-som-product-configurator.md)

