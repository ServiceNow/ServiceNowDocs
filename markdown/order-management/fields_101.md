---
title: Configure fields
description: Learn about how fields in CPQ help structure data collection efficiently and about the various types of field. Associate fields with blueprints for consistent use across configurations, layouts, and rules.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Configure fields

Learn about how fields in CPQ help structure data collection efficiently and about the various types of field. Associate fields with blueprints for consistent use across configurations, layouts, and rules.

A field is a designated space where users can enter specific information. Imagine fields as sections in a questionnaire, each awaiting a particular piece of data.

The usefulness of fields lies in their ability to structure data collection, making it easier for both users to enter values and admins to set them up efficiently and effectively. Without fields, the process of gathering information would be a chaotic jumble of function parameters, lacking the coherence necessary for meaningful data storage or the ability to enact rules.

In CPQ, fields are global. This means a field may be reused in any blueprint, rule, or layout without having to create a unique field for each.

-   [Layouts](layout_csv_101.md)
    -   Fields are the most granular component that make up a layout. A layout consists of many fields arranged into a navigational flow or page.
    -   Tabs, expandable sections, column sets, field grids, and headings provide additional organization to the fields in a configuration experience.
-   [Rules](rules_101.md)
    -   Rules leverage fields as inputs to conditions, calculations, and logic.
    -   Rules act on fields. A rule may determine the value of a field, display a message associated with a field, hide a field, control the options available in a field, and send the information in a field to the Product List, all in the same rule.
-   [Blueprints](blueprints_101.md)
    -   Because fields are global across an environment, the only way for them to be a part of a specific configuration is to be associated with a blueprint.
    -   When all of the fields referenced by a rule are associated with a blueprint, the rule is associated with the blueprint without the need to specify it.
    -   When a field is associated with a blueprint, the field can be added to the layouts of the blueprint.

When you associate a field to a blueprint, the application automatically associates all rules that leverage the field to the same blueprint. Fields and rules may be reused on any number of blueprints.

## Field types

Many field types are available, each with constraints and rules for entered values. For example, a number field is more suitable than a text field as a quantity field, since the only inputs it accepts are numbers.

Similarly, if there are only a few options that a user should be allowed to enter, a picklist field should be used to limit the options for the end user.

Because fields are global across an environment, all fields need a unique variable name when they are created. They can also be set as required during configuration, so that if the field is associated with a blueprint, it must be filled out before the configuration can be saved.

Text fields accept any characters entered into the field up to 2000 characters. The field definition allows the admin to specify minimum and maximum field lengths and a static default value.

![Activities screen](../images/cpq-text-field-options.png)

Numbers fields accept only numeric characters in their fields. The field definition requires the admin to specify whether the field will be used as a number, currency, or percentage. Optional settings include minimum and maximum values and a default value. The unit label setting is not currently used in the application.

![Admin screen](../images/cpq-number-field-options.png)

To specify the display precision of a numeric value, in the CPQ layout, click the gear icon in the number field. Then, set the precision in the Display Precision field.

![Field properties](../images/cpq-layout-field-properties-with-precision.png)

Boolean fields accept only two values: true and false. The field definition allows the admin to specify a true label, a false label, and a default value. Unless specified, the default true label is Enabled and the default false label is Disabled. The default state is false.

![A toggle switch with two options, “Enabled” and “Disabled,” showing a Boolean field set to False by default.](../images/cpq-fields-boolean.png)

Picklists are fields that only allow specified options to be selected, such as catalog items. When defining the field, the admin must specify whether the field is single-select, where the user must select one value, or multi-select, where the user can select as many values as desired. If the field is single-select, the admin must also specify whether the option values should be evaluated as a text field or a number field. The admin can also add field options, set an order, or a default value or values, and add picklist extension data if necessary.

![Picklist](../images/cpq-fields-picklist.png)

A product picker is like a picklist with extended data. product pickers can add products to a bill of materials and map additional data to product list fields, including extended data, without writing standard rules.

![Picklist picker](../images/cpq-fields-product-picker.png)

A set is a collection of fields that interacts only with the fields in their own row and column.

![Blueprint fields](../images/cpq-fields-sets.png)

## Sample blueprint showing field options and display variations

The following blueprint includes all the different field options and display variations. This ZIP file contains the layout CSV files that show how to set the component display types for each option.

[Component Display type blueprint](https://drive.google.com/file/d/1gq0Cc6ymPstowbT4xAg4M0GI8VlE9apj/view?usp=sharing)

**Related topics**  


[CPQ fields, system fields, and partner fields](system_fields_vs_partner_fields.md)

[Field type display options](field-type-display-options.md)

[Grid-style fields and field collections](what_field_type_should_i_use_for_organizing_field_options_and_data.md)

[Boundaries and limits](boundaries-and-limits.md)

