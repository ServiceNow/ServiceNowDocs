---
title: Dot-walkable Currency Instance fields
description: You can dot-walk certain fields in the Currency Instance \[fx\_currency2\_instance\] record, and field values stored in the database are consistent with each other. However, in script, since fields can be changed individually, and you change only some of the fields, they can be inconsistent.
locale: en-US
release: xanadu
product: Currency Administration
classification: currency-administration
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Currency administration references, Currency administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Dot-walkable Currency Instance fields

You can dot-walk certain fields in the Currency Instance \[fx\_currency2\_instance\] record, and field values stored in the database are consistent with each other. However, in script, since fields can be changed individually, and you change only some of the fields, they can be inconsistent.

## Currency code

The **Currency** field isn't a reference field, so you can set it to any value. However, if you enter an invalid currency code, an exception message is generated. An empty value is considered a session currency code.

## Query conditions

You can add query conditions on dot-walked fields in the instance table. However, when the query condition value is in a special format with currency code and amount, it's treated as a compound condition on the dot walked fields. The value has to be in format `XYZ,abc` where:

-   `XYZ` is a currency code, and
-   `abc` is an amount.

For example, `USD, 12.34`.

A condition such as `cost>USD,12.34` is treated as `cost.currency>USD AND cost.amount12.34`.

When the second operand is another Currency2 field, the condition translates in a similar manner:

`cost1>cost2` is treated as `cost1.currency=cost2.currency AND cost1.amount>cost2.amount`.

**Parent Topic:**[Currency administration references](currency-admin-references.md)

**Related topics**  


[Life cycle of records containing FX Currency fields](fx-currency-records-lifecycle.md)

