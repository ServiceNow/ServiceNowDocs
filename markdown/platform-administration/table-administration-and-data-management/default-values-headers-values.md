---
title: Default values for column headers and column values
description: Default values are used for column headers and column values, unless overridden by query parameters, Export Set fields, or system properties.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/table-administration-and-data-management/default-values-headers-values.html
release: zurich
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data export reference, Exporting data, Tables and data, Configure core features, Administer]
---

# Default values for column headers and column values

Default values are used for column headers and column values, unless overridden by query parameters, Export Set fields, or system properties.

The following table describes the default values used if you do not use query parameters, Export Set fields, or system properties to control output format.

|Output format|Column headers|Column values|
|-------------|--------------|-------------|
|CSV|**Use field name**|**Use raw value** if **glide.export.csv.raw.value** set, otherwise **Use display value**.|
|Excel|**Use field label**|**Use display label**|
|JSON|N/A|**Use raw value**|
|XLSX|**Use field label**|**Use display value**|
|XML|N/A|**Use raw value**|

**Parent Topic:**[Data export reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/table-administration-and-data-management/data-export-reference.md)

