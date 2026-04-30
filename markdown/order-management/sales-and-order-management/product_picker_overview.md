---
title: Product pickers
description: Learn how to create and configure product pickers to add products to a bill of materials \(BOM\) without writing rules. Define product options, subfields, aggregates, and display settings to enhance user interactions, automate data mapping, and present product information directly in layouts.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 7
breadcrumb: [ServiceNow CPQ Configurator, ServiceNow CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Product pickers

Learn how to create and configure product pickers to add products to a bill of materials \(BOM\) without writing rules. Define product options, subfields, aggregates, and display settings to enhance user interactions, automate data mapping, and present product information directly in layouts.

A product picker is similar to a picklist with extended data. product pickers can add products to a bill of materials and map additional data to product list fields, including extended data, without writing standard rules. Bulk actions provide additional, table based rules that can be used with the product picker Field.

## Creating a new product picker

Product Pickers can be created in the fields tab of the Logik Admin. To make a new product picker functional, all you need to do is add some options, then place it on a Layout. Select product picker as the new field type.

![New product picket](../images/cpq-product-picker-tile.png)

## Options

![Product picket options](../images/cpq-product-picker-setup.png)

Just like picklists, product pickers have a list of options. Each option represents a product, which is added to the BOM when selected by the user.

\(1\) The Product Options tab is the starting point for adding options to the product picker. Options are displayed below in table format.

Product Picker Option Fields:

-   \(2\) Order: display order of options in the product picker
-   \(3\) Name: name to use for the product picker option \(required\)
-   \(4\) Value: value to use for the product picker option \(required, defaults to name\)
-   \(5\) imageUrl: URL of an image to use for this product picker option
-   \(6\) defaultValue: Controls if this option is selected by default

Actions:

-   \(7\) Add Row: Add product picker
-   \(8\) Delete: Delete the selected options of the product picker options table
-   \(9\) Save options

## Option import

Product Picker options can be imported directly into the Picker by uploading a CSV file, much like picklist options.

![Product picker setup](../images/cpq-product-picker-option-import.png)

-   \(1\) Menu: Click the 3 vertical dot icon to open the menu
-   \(2\) Import product picker options: launch the import dialog for product picker options
-   \(3\) Delete Selected options: If any product picker options are selected, delete them

Import dialog:

![Import options](../images/cpq-product-picker-csv-import.png)

\(1\) CSV import: Click or drag and drop the CSV file containing the product picker options that you want to import.

\(2\) Import: Once a file is selected, click import to load the options into the product picker.

## Product Picker fields

Fields can be created in the product picker and used to collect user input, interact with rules, display information and optionally set data in the product list. These fields are children of the current product picker and are found in the Option Fields tab. They are also referred to as subfields.

![Product picker fields](../images/cpq-product-picker-fields.png)

\(1\) Option Fields tab: Additional subfields can be created and added to the product picker to display and optionally pass additional data into the ProductList. Subfields are displayed in a table format below.

Three fields are automatically included in each product picker:

-   \(2\) Value: the value of the option, by default maps to Product Id when selected
-   \(3\) Select: Boolean field that controls if the product option is added to the product list \(BOM\)
-   \(4\) Quantity: quantity of the product to add when option is selected, by default maps to Product Quantity

Additional subfields can be created and optionally configured to pass additional data into the ProductList or display in the UI.

-   \(5\) Field Type: Can be Text, Number, Boolean or Picklist
-   \(6\) Field Name
-   \(7\) Variable Name: Variable name of new subfield, including the product picker variable name as the prefix
-   \(8\) ProductList property: Optionally, you can configure the newly created field to pass data into the ProductList. Select the field in the ProductList to map the subfieldʼs value to, or choose None to not pass the data

## Aggregates

Aggregates can be created on product pickers, similar to how set aggregates work. For information about set aggregates, see [Creating set aggregates](creating_set_aggregates.md).

## Setup

![Product picker setup](../images/cpq-product-picker-setup-2.png)

Navigate to a product picker field.

-   \(1\) Open the Option Fields tab in the product picker
-   \(2\) New section for aggregate fields
-   \(3\) Add button to create a new aggregate field

![Select picker value screen](../images/cpq-product-picker-new-aggregate-field.png)

When you create a new aggregate field, you can select any of the subfields in a product picker to aggregate on.

A list of available sub fields are displayed. Select the field to create a new aggregate.

![Picker options screen](../images/cpq-product-picker-new-aggregate-subfield.png)

1. Five types of aggregates can be created:

-   Sum
-   Average
-   Min
-   Max
-   Count

Select the aggregate type to use for the subfield. Each aggregate type can only be used once per subfield.

![Aggregate fields screen](../images/cpq-product-picker-aggregate-type.png)

Final Aggregate Field:

-   \(1\) Subfield to aggregate on
-   \(2\) Aggregate Type
-   \(3\) Field Name \(automatically generated\)
-   \(4\) Variable Name \(automatically generated\)
-   \(5\) Delete

## Example

Aggregate fields can be added to the layout and will automatically be calculated on change of a field.

![Simple product picker screen](../images/cpq-product-picker-aggregate-example.png)

-   \(1\) Quantity Max = 3, product b has qty 3
-   \(2\) Quantity Sum = 4, one product with qty 1, one with qty 3
-   \(3\) Select Count = 2, 2 products are selected

## Product Info fields

Product Pickers can optionally display some read-only information about a product. The values are pulled from the product template that is cached in Logik. These fields can then be added to the layout.

**Note:** These values are read-only and cannot be set by rules.

![Product info fields](../images/cpq-product-picker-read-only-information.png)

-   \(1\) Available fields: Any available fields will be editable, to include a field and make it available in the layout, check the box next to the field name
-   \(2\) Unavailable fields: Fields that are mapped to a subfield will be grayed out and unavailable to be included. To make a field available again, change the mapping of the subfield in the product picker Fields section

## Product Picker settings

![Product picker settings screen](../images/cpq-product-picker-settings.png)

Product pickers have additional properties that can be set, both to control the product picker behavior itself and to set additional default values for the product list.

-   \(1\) product picker Settings: Click the gear icon to open the product picker Settings menu
-   \(2\) Type: Single-select or multiselect product picker, behaves same as picklist
-   \(3\) Sync Selected field with Quantity: Boolean toggle field that controls whether the Quantity and Select fields in the Product picker are kept in sync. If enabled, these values are set based on whether the user has made changes. See the scenarios listed in the table below.
-   \(4\) Enable for Pricing Enrichment: enable the product picker for Pricing Enrichments
-   \(5\) Type: Type to use for product options, Accessory or Component
-   \(6\) BOM Type: Which BOM to set by default for the product options
-   \(7\) Parent Product: Name of the parent product to use by default for the product options

This table shows scenarios where the user changes Quantity and Logik changes Select, or vice versa. In all other cases, the value is not changed.

|Change|Status of Quantity field|Status of Select field|Result|
|------|------------------------|----------------------|------|
|User changes Select to false|Set to non-zero by rule| |Quantity set to 0|
|User changes Select to true|Set to 0 by user| |Quantity set to 1 \(or its min value\)|
|User changes Select to true|Set to 0 by rule| |Quantity set to 1 \(or its min value\)|
|User changes Quantity to non- zero| |Set to false by user|Select set to true|
|User changes Quantity to non- zero| |Set to false by rule|Select set to true|
|User changes Quantity to 0| |Set to true by user|Select set to false|
|User changes Quantity to 0| |Set to true by rule|Select set to false|

## Product Pickers in layouts

Product Pickers can be added and edited in Layouts both through the Layout Wizard and through the Layout CSV. Four basic display types are supported:

-   VisualProductPicker: Tile based display, Single-select
-   MultiSelectVisualProductPicker: Tile based display, multiselect
-   ProductPickerGrid: Table based display, Single-select
-   MultiSelectProductPickerGrid: Table based display, multiselect

![Visual picker screen](../images/cpq-product-picker-visual-product-picker.png)

## Product Picker imports and exports

If a product picker Field is associated with a blueprint, it will be included in the exports of that blueprint.

From the Fields page in the ServiceNow CPQ Admin, select a product picker to export and a ZIP file will be generated containing the following:

-   Product Picker fields
-   Product Picker field options
-   Product Picker definition and bulk actions
-   Bulk Action data, each in a CSV file

A ZIP file containing a product picker can be imported through the Matrix Loader.

**Related topics**  


[Product picker bulk actions](product_picker_bulk_actions.md)

[Referencing a product picker](enrichments_how_to_reference_a_product_picker.md)

