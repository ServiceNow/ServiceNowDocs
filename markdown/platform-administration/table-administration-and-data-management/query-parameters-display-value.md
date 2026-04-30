---
title: Query parameters for display value and header
description: Use query parameters to export the display value or raw value of fields and the field label or field name for headers.
locale: en-US
release: xanadu
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2024-08-01"
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

Exports the display value \(**true**\) or raw value \(**false**\) for the CSV, XLS, XLSX, and XML file formats.See [Field types affected by export controls](../reference/field-types-affected.md) for more information.

</td></tr><tr><td>

**displayvalue**

</td><td>

Exports the display value \(**true**\), raw value \(**false**\), or both \(**All**\) for the JSON file format.See [Field types affected by export controls](../reference/field-types-affected.md) for more information.

</td></tr><tr><td>

**sysparm\_export\_column\_header\_label**

</td><td>

Exports the CSV, XLS, and XLSX file formats with the field label \(**true**\) or field name \(**false**\).

</td></tr></tbody>
</table>## sysparm\_display\_value

-   **Example: __sysparm\_display\_value__ = __true__**

    ![Example: sysparm_display_values = true](../image/XLSX-sysparm-display-value-true.png)

-   **Example: __sysparm\_display\_value__ = __false__**

    ![Example: sysparm_display_values = false](../image/XLSX-sysparm-display-value-false.png)


## displayvalue

-   **Example: __displayvalue__ = __true__**

    ![Example: displayvalue = true](../image/json-displayvalue-true.png)

-   **Example: __displayvalue__ = __false__**

    ![Example: displayvalue = false](../image/json-displayvalue-false.png)

-   **Example: __displayvalue__ = __All__**

    ![Example: displayvalue = all](../image/json-displayvalue-all.png)


## sysparm\_export\_column\_header\_label

-   **Example: __sysparm\_export\_column\_header\_label__ = __true__**

    ![Example: sysparm_export_column_header_label = true](../image/sysparm_export_column_header_label-true.png)

-   **Example: __sysparm\_export\_column\_header\_label__ = __false__**

    ![Example: sysparm_export_column_header_label = false](../image/sysparm_export_column_header_label-false.png)


**Parent Topic:**[Data export reference](../reference/data-export-reference.md)

