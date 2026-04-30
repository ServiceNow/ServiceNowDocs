---
title: System properties for Reports
description: The system properties for reports are explained below.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Report Templates, Administration, Threat Intelligence Security Center, Security Operations]
---

# System properties for Reports

The system properties for reports are explained below.

<table id="table_u5p_fhy_hbc"><thead><tr><th>

Property

</th><th>

Description

</th><th>

Value

</th></tr></thead><tbody><tr><td>

sn\_sec\_reporting.max\_list\_columns\_allowed

</td><td>

Limit the number of columns which can be added when rendering lists in report pdfs. This will use the columns from the beginning from the view till the allowed limit.

</td><td>

5

</td></tr><tr><td>

sn\_sec\_reporting.report\_default\_style\_object

</td><td>

Use this property to control css of free form fields, left panel, report lists.

</td><td>

\(JSON object\)

</td></tr><tr><td>

sn\_sec\_reporting.load\_all\_records

</td><td>

Loads all the records for the lists in the report created from a template. true - Load all records and false - loads specific number of records defined by sn\_sec\_reporting.reporting\_list\_records\_count property.

</td><td>

False

</td></tr><tr><td>

sn\_sec\_reporting.reporting\_list\_records\_count

</td><td>

Loads specific number of records in the report editor.

</td><td>

20

</td></tr><tr><td>

sn\_sec\_tisc.sn\_sec\_tisc\_case.defang\_record\_list\_urls

</td><td>

Controls whether URLs from lists will be defanged or not.

</td><td>

True

</td></tr><tr><td>

sn\_sec\_tisc.show\_all\_tactics\_reporting

</td><td>

If true, shows all tactics \(including the tactics which doesn't have any techniques associated to the case\) for the MITRE lists rendered in the report.

</td><td>

False

</td></tr><tr><td>

sn\_sec\_tisc.reporting\_email\_template\_sn\_sec\_tisc\_case

</td><td>

Sys ID of the email client template for the Case \(sn\_sec\_tisc\_case\) table which will be used in share report.

</td><td>

b55e22c54324021060eee0ea78b8f2df

</td></tr><tr><td>

sn\_sec\_tisc.sn\_sec\_tisc\_case.excluded\_ctx\_fields

</td><td>

Excluded fields of the case in the report/template menu options for substituting a field.

</td><td>

\(List of all excluded case fields

</td></tr><tr><td>

sn\_sec\_tisc.sn\_sec\_tisc\_case.ctx\_menu\_field\_header

</td><td>

This property is used to get the corresponding UI message record for the case fields label in the report/template menu options.

</td><td>

sn\_sec\_tisc\_case\_reporting\_ctx\_menu\_field\_header

</td></tr></tbody>
</table>