---
title: Default currency values in import and export
description: In general, currency values crossing the boundaries of the platform are represented in the user’s session currency and formatted in the user’s locale.
locale: en-US
release: zurich
product: Currency Administration
classification: currency-administration
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Standard currency fields, Explore, Currency administration, Configure core features, Administer]
---

# Default currency values in import and export

In general, currency values crossing the boundaries of the platform are represented in the user’s session currency and formatted in the user’s locale.

## Import

Currency values are imported as strings, just like other fields. The default transform mapping to a currency field uses setDisplayValue\(\). The expected format for this function is:

-   A number formatted in the user’s locale. The number is taken as a value in the user's session currency, for example, 1,234.56.
-   The number prefixed by the three-letter currency code separated by a semicolon, for example, EUR;1.234,56.

This behavior can be customized in transform map scripts.

## Export

Currency values can be exported in several formats, including CSV, XLSX, PDF, and XML. Depending on the export format, currency values are exported in the user’s session currency and formatted in the user’s locale or they're exported in the reference currency value with no formatting.

**Parent Topic:**[Standard currency fields](configure-and-use-default-currency-fields.md)

**Related topics**  


[Exporting currency fields to Excel](../../exporting-data/concept/c_ExportingCurrencyFields.md)

