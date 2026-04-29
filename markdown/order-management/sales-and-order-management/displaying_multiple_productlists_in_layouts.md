---
title: Displaying multiple product lists in layouts
description: You can configure multiple product lists for a single layout by creating and importing a layout CSV file.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ProductList.Type options: Accessory and Component, CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Displaying multiple product lists in layouts

You can configure multiple product lists for a single layout by creating and importing a layout CSV file.

In CPQ, a layout can show multiple bills of material \(BOMs\) at once. This can help separate different types of products or separate sales items from manufacturing details.

**Note:** To display in different BOMs, products must have different BOM types. By default, products whose BOM type is not `sales` are not created as a quote line when going through Salesforce CPQ.

Use the BOM Types to Include in Save Request admin setting to add additional BOM types to a Save request. Any BOM types added here are passed in the save request and created as quote lines when going through Salesforce CPQ.

Use the Push BOM Data to Logik Salesforce Object admin setting to configure BOM items to be passed back and written into Salesforce as configuration line items.

To learn how to add additional BOM types to a Save request and to configure BOM items to be written to Salesforce as configuration line items, see [CPQ admin settings](cpq-admin-settings.md).

To add multiple product lists to a layout, use tiers to separate the additional BOMs. Product lists can be added by editing the layout CSV file and importing it. For information about displaying multiple BOMs in a layout, view the following video:

[Multiple BOM Display](https://www.youtube.com/watch?v=e9xylvbnLgk)

## Multiple bills of material: CSV setup

![CSV setup](../images/cpq-multiple-boms-csv-setup.png)

1.  The first product list uses the same format as the default product list included in layouts
2.  The value for this product list determines that this will display in a modal window and with type:all will contain all of the BOM items
3.  The second product list is the manufacturing BOM, now contained in a tier as indicated in the type and path fields
4.  Variable names are required to construct the path for the layout to render correctly
5.  The complete path for columns is in the format `/layout/tiers/<tierVariableName>/<productListVariableName>/columns`
6.  The value for this product list component does not have a location, as it is in a tier. "type":"manufacturing" will include all products with the manufacturing bomType. The total field for this product list is also hidden with "totalLocation": "none"
7.  The third product list component is the sales BOM, and repeats most of the manufacturing BOM product list

See this [sample layout CSV](https://docs.google.com/spreadsheets/d/1vTouzEdkHaBv9ddTN5UyB8Gm4BugymaDNfnTS86xaME/edit?usp=sharing).

## Multiple bills of material: layout editor

![CSV setup](../images/cpq-multiple-boms-layout-editor.png)

1.  Display of the manufacturing BOM product list in the layout editor in a tier
2.  Display of the sales BOM product list in the layout editor in a tier
3.  Display of the Complete \(all\) product list in the layout editor as a modal window

## Final configuration experience

![CSV setup](../images/cpq-multiple-boms-final-config.png)

1.  Manufacturing product list, only displaying the manufacturing bomType products
2.  Sales BOM product list, only displaying the sales bomType products
3.  The complete list in a new window set to show all the products from any bomType

**Related topics**  


[Customizing the currency display in the shopping cart](layout_how_do_i_customize_currency_display_in_shopping_cart.md)

