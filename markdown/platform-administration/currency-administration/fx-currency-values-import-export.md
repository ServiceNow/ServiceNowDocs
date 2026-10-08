---
title: FX Currency values in import and export
description: Updated with Claude for DOC1141697.FX Currency values that you import must include a three-letter ISO currency code, a semicolon, and an amount formatted for the user's locale, such as USD;1,234.56. In general, imported and exported values represent the display value returned by getDisplayValue.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/currency-administration/fx-currency-values-import-export.html
release: brazil
product: Currency Administration
classification: currency-administration
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [FX Currency fields, Explore, Currency administration, Configure core features, Administer the ServiceNow AI Platform]
---

# FX Currency values in import and export

FX Currency values that you import must include a three-letter ISO currency code, a semicolon, and an amount formatted for the user's locale, such as `USD;1,234.56`. In general, imported and exported values represent the display value returned by `getDisplayValue`.

## FX Currency import

If using the default `setDisplayValue()` import method, FX Currency works in a manner similar to the standard currency field. It imports a value such as `USD;1,234.56` as `setDisplayValue("USD;1,234.56")`. It then parses the value as a three letter ISO currency code, followed by a semi-colon, followed by a number formatted in the locale of the user. The currency code is required. FX Currency values are imported as display value strings, so each value in the source file must include the code. For example, to import 100 US dollars from an Excel file, enter `USD;100` in the source column. If you import only a number, such as `100`, the value might not be imported. This method should work for most use cases.

Defaults for other Currency Instance fields come from FX Currency field configuration you defined in **System Localization** &gt; **FX Currency Configuration**. To explicitly set these fields, you can use a custom import script that sets those fields to desired values, possibly using values from another import column.

There are various ways to import FX Currency data.

<table id="table_vqg_pmv_5jb"><thead><tr><th>

Method

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Importing data into custom rate tables

</td><td>

Main method for importing custom rates, other than editing rates directly. When you modify existing rates, existing currency values that use that rate aren't updated.

 **Note:** This is specific for importing only.

</td></tr></tbody>
</table>## FX Currency export

There are various ways to export FX Currency data.

<table id="table_rx3_mlv_5jb"><thead><tr><th>

Method

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show XML

</td><td>

Shows an XML file with instance records for each FX Currency field bundled inside the XML payload.

</td></tr><tr><td>

Export to XML

</td><td>

Shows an unload XML with unloads for all instance records.

</td></tr><tr><td>

Export to Excel/PDF

</td><td>

Uses the default method of exporting data that extracts data from fields using `getDisplayValue()`. For FX Currency fields, using this method returns a formatted currency string of the form $1,234.56. To access specific information inside an FX Currency field directly without any transformations, simply export that column using dot walking.

</td></tr></tbody>
</table>**Parent Topic:**[FX Currency fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/currency-administration/fx-currency.md)

