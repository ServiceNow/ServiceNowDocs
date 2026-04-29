---
title: Control default currency field configuration and use in an instance
description: You can control how currency fields are configured and used in your instance.
locale: en-US
release: australia
product: Currency Administration
classification: currency-administration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Defaults required for standard currency use, Configure, Currency administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Control default currency field configuration and use in an instance

You can control how currency fields are configured and used in your instance.

These properties are available for currency fields.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_rv2_c1t_gx"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.sys.audit\_currency\_value**

</td><td>

When **true**, currency fields in audit records are the value entered by the user, in the format `USD;1234.56`. When **false**, the value is the numeric value in the session currency.-   Type: Boolean
-   Default value: **false**
-   Location: System Property \[sys\_properties\] table
-   Learn more: [Configure default currency fields in audit records](../task/audit-currency-fields.md)

</td></tr><tr><td>

**glide.currency\_price.use\_all\_fraction\_digits**

</td><td>

When **true**, currency fields have four decimal places. When **false**, two decimal places are used.-   Type: Boolean
-   Default value: **false**
-   Location: System Property \[sys\_properties\] table
-   Learn more: [Change default currency decimal places](../task/change-currency-fraction-digits.md)

</td></tr><tr><td>

**glide.currency\_price\_optimizer.enabled**

</td><td>

When **true**, the optimizer is used. When **false**, the optimizer is not used.-   Type: Boolean
-   Default value: **true**
-   Location: System Property \[sys\_properties\] table
-   Learn more: [Configure the currency optimizer](../task/configure-currency-optimizer.md)

</td></tr><tr><td>

**glide.currency\_price\_optimizer.min\_rows**

</td><td>

Minimum number of rows in parent table needed for the optimizer. When fewer than this number of rows are present, the optimizer is not used.-   Type: Number
-   Default value: **4**
-   Location: System Property \[sys\_properties\] table
-   Learn more: [Configure the currency optimizer](../task/configure-currency-optimizer.md)

</td></tr><tr><td>

**glide.excel.convert\_to\_user\_currency**

</td><td>

When **true**, currency fields in a table are output in the user's session currency.-   Type: Boolean
-   Default value: **false**
-   Location: System Property \[sys\_properties\] table
-   Learn more: [Exporting currency fields to Excel](../../exporting-data/concept/c_ExportingCurrencyFields.md)

</td></tr><tr><td>

**glide.excel.fixed\_currency\_usd**

</td><td>

When **true**, currency fields in a table are converted to US dollars.-   Type: Boolean
-   Default value: **false**
-   Location: System Property \[sys\_properties\] table
-   Learn more: [Exporting currency fields to Excel](../../exporting-data/concept/c_ExportingCurrencyFields.md)

</td></tr><tr><td>

**glide.system.locale**

</td><td>

Value is of the format `Language.Country` where the language is an ISO 639 language code and the country is an ISO 3166 language code. Internally, this value is used as specified by Java. The system locale setting should be in the [Java supported locales](http://www.oracle.com/technetwork/java/javase/javase7locales-334809.html) list.-   Type: String
-   Default value: empty
-   Location: **System Properties** &gt; **System Localization**
-   Learn more: [Locale settings](../concept/locales.md)

</td></tr></tbody>
</table>**Parent Topic:**[Setting up defaults required for standard currency use](../concept/setting-up-standard-currency-defaults.md)

**Related topics**  


[Exporting currency fields to Excel](../../exporting-data/concept/c_ExportingCurrencyFields.md)

