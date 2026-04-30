---
title: Understanding FX Currency values in forms
description: In forms, the FX Currency field behaves like a dot walkable field in script. It consists of an entry field, and an accompanying list for selection of a currency code.
locale: en-US
release: yokohama
product: Currency Administration
classification: currency-administration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [FX Currency fields, Exploring currency administration, Currency administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Understanding FX Currency values in forms

In forms, the FX Currency field behaves like a dot walkable field in script. It consists of an entry field, and an accompanying list for selection of a currency code.

Specifically, FX Currency fields that appear on forms contain the following: ![Fx currency field](../images/currency2-field.png)

-   An empty field for entry of a numeric currency value, formatted according to your assigned user locale. For example, in the US, it is formatted with two decimal places, for entry of cents.

    If this is a new record, the field is empty. If it is an existing record, the previous currency amount that you entered appears.

-   A selection list of active currencies from the Currency \[fx\_currency\] table. The default currency code is based on your user locale. You can select another currency for use during the entry session.

    For example, in the US, the default currency value, based on the user locale, is USD. You can select another currency code to use in the current entry session.

-   An edit icon \(![Edit icon](../images/currency-edit.png)\). Users with an assigned currency\_instance\_admin role can click it to edit currency detail in the accompanying Currency Instance \[fx\_currency2\_instance\] record.

**Parent Topic:**[FX Currency fields](fx-currency.md)

