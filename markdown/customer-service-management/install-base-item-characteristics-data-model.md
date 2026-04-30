---
title: Data model for the Install base item characteristics
description: The data model for the install base item characteristics represents how the characteristics of an install base item are stored in the Customer Service Management application. The data model refers to the characteristic values and options and provides a view of how to store a set of characteristics associated to an install base item.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Install base characteristics, Install base items, Configure install base, Configure product data, Product data, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Data model for the Install base item characteristics

The data model for the install base item characteristics represents how the characteristics of an install base item are stored in the Customer Service Management application. The data model refers to the characteristic values and options and provides a view of how to store a set of characteristics associated to an install base item.

The Customer Service Management application has several functional and granular roles that provide access levels to create, read, and update characteristics for an install base item. The install base item characteristics table \[sn\_install\_base\_item\_characteristic\] comes with different security roles and plugins. For more information on security roles, see [Security roles for the install base characteristics](security-roles-for-install-base-attributes.md).

The following diagram shows the data model for the Install base characteristics. The data model represents the new and existing install base item and install base item characteristics tables.



![Install base item characteristics data model. For the text description, refer to the section that preceded this diagram.](../image/ib-characteristics-data-model.png)

The following table describes the different fields on the Install base characteristics form.

<table id="table_f3b_k1p_5xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Characteristic

</td><td>

Characteristic that is associated with the install base item.

</td></tr><tr><td>

Characteristic option

</td><td>

Characteristic option that you chose from a list of options for the selected characteristic.

**Note:** This field is available when the characteristic that you select is a choice, Boolean, or check box type of option.

</td></tr><tr><td>

Value

</td><td>

String value for the selected characteristic.

**Note:** This field is available when the characteristic that you select expects a string input and isn't a choice, Boolean, or check box type of option.

</td></tr><tr><td>

Install base item

</td><td>

Install base item that the characteristics are added to.

</td></tr></tbody>
</table>