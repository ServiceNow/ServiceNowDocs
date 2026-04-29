---
title: Price fields
description: A price field is a currency field that enables control over conversions and display.
locale: en-US
release: australia
product: Currency Administration
classification: currency-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Standard currency fields, Explore, Currency administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Price fields

A price field is a currency field that enables control over conversions and display.

You can select conversion and display options per price field, and change them at any time. There are three variations:

-   **Calculated \[Default\]**

    Behaves in the same way as the default currency field type. Whenever conversions are performed, it uses the latest currency conversion rates. The price field appears in the session currency for the user.

-   **Fixed**

    When the price field appears, it is shown in the currency code used when you entered the value. Whenever conversions are performed, it uses the latest currency conversion rates.

-   **Multiple**

    Enables you to enter multiple price values for an item using a different currency for each price. The field value is the value entered in the user’s session currency. Otherwise, the first price entered converts to the user’s session currency. Whenever conversions are performed, it uses the latest currency rates.

    **Note:** The first value entered is used during display. The additional values are not used during calculations.


You can change the currency code and numeric value for a price field. When you click the **Edit** icon that appears next to the price field, a form appears that you use to edit the details for the price field:

<table id="table_b1r_nnk_4jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Currency

</td><td>

List of currencies enabled in the system in the combo box. In single currency mode, the currency is a label and cannot be changed.

</td></tr><tr><td>

Amount

</td><td>

Numeric value formatted in the user’s locale.

</td></tr><tr><td>

Type

</td><td>

Calculated, Fixed, Multiple.-   When you change the price type to Multiple, the system creates child records for all currencies enabled in the platform. The child records are populated with values converted from the amount field, using latest currency conversion rates.
-   You cannot change the price type in single currency mode.
-   You can modify the price type at any time.

</td></tr></tbody>
</table>**Parent Topic:**[Standard currency fields](configure-and-use-default-currency-fields.md)

