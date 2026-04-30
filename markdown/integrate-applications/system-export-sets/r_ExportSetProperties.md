---
title: Export Set properties
description: Multiple properties control export set behavior.
locale: en-US
release: zurich
product: System Export Sets
classification: system-export-sets
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Export sets, Exports, Workflow Data Fabric]
---

# Export Set properties

Multiple properties control export set behavior.

<table id="table_cyp_3dk_qr"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.excel.local\_based\_currency**

</td><td>

For Excel files, option to format currency values to match the localization of the instance.

 For example, say you've activated the I18N: French Canada Translations plugin on your instance, and you're exporting a currency value of 6300. If this property is set to true, the value will be correctly formatted as 6,300 €. If this property is set to false, the value will be formatted as € 6,300.

 For more information on localization, see [Localization Framework](https://www.servicenow.com/docs/access?context=localization-framework-landing&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

 -   Type: true \| false
-   Default: false
-   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)

</td></tr><tr><td>

**glide.export.excel.duration.readable\_string**

</td><td>

For Excel files, option to format duration fields in days, hours, minutes, and sometimes, seconds.

 When false, duration fields are given in seconds. For example, the **Actual elapsed time** field might have a value of 191,760 seconds.

 When true, duration fields are formatted in days, hours, and minutes. For example, the **Actual elapsed time** field mentioned previously would have a value of 2 Days, 5 Hours, and 16 Minutes.

 In some situations, duration fields include seconds, even when this property is true. This happens when the duration is less than one minute, or when the system property **glide.ui.duration.seconds.enabled** is true.

 -   Type: true \| false
-   Default: false
-   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)

</td></tr><tr><td>

**glide.export.xlsx.zip64\_mode**

</td><td>

For XLSX files, controls the compression mode. When true, XSLX files are generated using the Zip64 algorithm.

 -   Type: true \| false
-   Default: false
-   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)

</td></tr><tr><td>

**glide.scheduled\_export.stop\_on\_parent\_error**

</td><td>

When true, if a parent scheduled export set encounters an error, scheduled child export sets don't run.-   Type: true \| false
-   Default: false
-   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)

</td></tr></tbody>
</table>