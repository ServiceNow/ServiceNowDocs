---
title: Query parameters for display value and header
description: Use query parameters to export the display value or raw value of fields and the field label or field name for headers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/table-administration-and-data-management/query-parameters-display-value.html
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data export reference, Exporting data, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Query parameters for display value and header

Use query parameters to export the display value or raw value of fields and the field label or field name for headers.

Query parameters control the output for CSV, XLS, JSON, XLSX, and XML file formats. Query parameters, if present, override system properties.

The following table describes each of the query parameters that control display values and headers.

<table id="table_ps3_vz3_hbb"><thead><tr><th>

Query parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sysparm\_display\_value**

</td><td>

Exports the display value \(**true**\) or raw value \(**false**\) for the CSV, XLS, XLSX, and XML file formats.See [Field types affected by export controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/field-types-affected.md) for more information.

</td></tr><tr><td>

**displayvalue**

</td><td>

Exports the display value \(**true**\), raw value \(**false**\), or both \(**All**\) for the JSON file format.See [Field types affected by export controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/field-types-affected.md) for more information.

</td></tr><tr><td>

**sysparm\_export\_column\_header\_label**

</td><td>

Exports the CSV, XLS, and XLSX file formats with the field label \(**true**\) or field name \(**false**\).

</td></tr></tbody>
</table>## sysparm\_display\_value

-   **Example: __sysparm\_display\_value__ = __true__**

    \[Omitted image "XLSX-sysparm-display-value-true.png"\] Alt text: Example: sysparm\_display\_values = true

-   **Example: __sysparm\_display\_value__ = __false__**

    \[Omitted image "XLSX-sysparm-display-value-false.png"\] Alt text: Example: sysparm\_display\_values = false


## displayvalue

-   **Example: __displayvalue__ = __true__**

    \[Omitted image "json-displayvalue-true.png"\] Alt text: Example: displayvalue = true

-   **Example: __displayvalue__ = __false__**

    \[Omitted image "json-displayvalue-false.png"\] Alt text: Example: displayvalue = false

-   **Example: __displayvalue__ = __All__**

    \[Omitted image "json-displayvalue-all.png"\] Alt text: Example: displayvalue = all


## sysparm\_export\_column\_header\_label

-   **Example: __sysparm\_export\_column\_header\_label__ = __true__**

    \[Omitted image "sysparm\_export\_column\_header\_label-true.png"\] Alt text: Example: sysparm\_export\_column\_header\_label = true

-   **Example: __sysparm\_export\_column\_header\_label__ = __false__**

    \[Omitted image "sysparm\_export\_column\_header\_label-false.png"\] Alt text: Example: sysparm\_export\_column\_header\_label = false


**Parent Topic:**[Data export reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/data-export-reference.md)

