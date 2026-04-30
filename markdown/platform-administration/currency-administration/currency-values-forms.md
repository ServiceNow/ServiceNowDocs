---
title: Default currency values in forms
description: In forms, currency values appear in the currency in which they were entered.
locale: en-US
release: zurich
product: Currency Administration
classification: currency-administration
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Standard currency fields, Explore, Currency administration, Configure core features, Administer]
---

# Default currency values in forms

In forms, currency values appear in the currency in which they were entered.

A combo box provides a list of available currencies, and the user's locale determines its format. When entering or changing the numeric currency value, enter it in the same format specified by the user’s locale. In the form for a new record, the reference currency is pre-selected in the currency list, with the numeric value set to zero.

![Currency combo box](../images/currency-field.png)

-   If the record is read only, the currency value appears in the **Currency** field as it was entered, and is formatted in the user’s locale. In the **Price** field, the session currency value appears.
-   In Single currency mode, the currency is a label that cannot be changed, and the **Edit** icon does not appear.

## Editing the currency instance record

If a currency instance record exists, an **Edit** icon appears next to the **Currency** field if you have edit rights for the fx\_currency\_instance table. Users with the financial\_mgmt\_user role can edit the values associated with the currency field.

**Note:** Normally, you should not edit the fx\_currency\_instance table directly. The ServiceNow AI Platform maintains these tables, and your changes could have unintended consequences.

**Parent Topic:**[Standard currency fields](configure-and-use-default-currency-fields.md)

