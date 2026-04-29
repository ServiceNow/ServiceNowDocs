---
title: System properties for TISC Reports
description: The following section describes the system properties applicable to TISC reports.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [About Report Templates in TISC, Administer Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# System properties for TISC Reports

The following section describes the system properties applicable to TISC reports.

<table id="table_u5p_fhy_hbc"><thead><tr><th>

Property

</th><th>

Description

</th><th>

Value

</th></tr></thead><tbody><tr><td>

sn\_sec\_tisc.sn\_sec\_tisc\_case.excluded\_ctx\_fields

</td><td>

Excluded fields of the case in the report/template menu options for substituting a field.**Note:** This limitation applies only to Case Reports.

</td><td>

List of all excluded case fields.

</td></tr><tr><td>

sn\_sec\_tisc.sn\_sec\_tisc\_case.ctx\_menu\_field\_header

</td><td>

This property is used to get the corresponding UI message record for the case fields label in the report/template menu options.**Note:** This limitation applies only to Case Reports.

</td><td>

sn\_sec\_tisc\_case\_reporting\_ctx\_menu\_field\_header

</td></tr><tr><td>

sn\_sec\_tisc.sn\_sec\_tisc\_case.load\_all\_records

</td><td>

Determines whether all records are loaded for lists in reports created from a template.-   **True**: Loads all records from the list into the report.
-   **False**: Loads only the number of records specified by the property `sn_sec_tisc.sn_sec_tisc_case.reporting_list_records_count`.

**Note:** This limitation applies only to Case Reports.

</td><td>

False

</td></tr><tr><td>

sn\_sec\_tisc.sn\_sec\_tisc\_case.reporting\_list\_records\_count

</td><td>

Loads specific number of records in the report editor.

</td><td>

20

</td></tr><tr><td>

sn\_sec\_tisc.sn\_sec\_tisc\_case.report\_default\_style\_object

</td><td>

This property is used to control the CSS for free-form fields, the left panel, and the report lists for Case reports.**Note:** This limitation applies only to Case Reports.

</td><td>

\(JSON object\)

</td></tr><tr><td>

sn\_sec\_tisc.sn\_sec\_tisc\_case.max\_list\_columns\_allowed

</td><td>

Defines the maximum number of columns that can be rendered when generating lists in case report PDFs. The application then includes the columns sequentially from the beginning of the view up to the specified limit. Any additional columns beyond this limit will be excluded from the rendered output.**Note:** This limitation applies only to Case Reports.

</td><td>

5

</td></tr><tr><td>

sn\_sec\_tisc.show\_all\_tactics\_reporting

</td><td>

If true, shows all tactics \(including the tactics which doesn't have any techniques associated to the case\) for the MITRE lists rendered in the report.**Note:** This limitation applies only to Case Reports.

</td><td>

False

</td></tr><tr><td>

sn\_sec\_tisc.sn\_sec\_tisc\_case.honor\_report\_lists\_column\_selection

</td><td>

Controls whether column selection should be honored when selecting records from lists during the editing of Case Reports.**Note:** This limitation applies only to Case Reports.

</td><td>

True

</td></tr><tr><td>

sn\_sec\_tisc.sn\_sec\_tisc\_case.defang\_record\_list\_urls

</td><td>

Controls whether URLs from lists will be defanged or not.**Note:** This limitation applies only to Case Reports.

</td><td>

True

</td></tr><tr><td>

sn\_sec\_tisc.intelligence\_report.report\_default\_style\_object

</td><td>

This property is used to control the CSS for free-form fields, the left panel, and the report lists for intelligence reports.**Note:** This limitation applies only to Intelligence Reports.

</td><td>

\(JSON object\)

</td></tr><tr><td>

sn\_sec\_tisc.intelligence\_report.max\_list\_columns\_allowed

</td><td>

Defines the maximum number of columns that can be rendered when generating lists in intelligence report PDFs. The application then includes the columns sequentially from the beginning of the view up to the specified limit. Any additional columns beyond this limit will be excluded from the rendered output.

**Note:** This limitation applies only to Intelligence Reports.

</td><td>

5

</td></tr><tr><td>

sn\_sec\_tisc.intelligence\_report.honor\_report\_lists\_column\_selection

</td><td>

Controls whether the column selection should be honored when selecting records from lists during the editing of Intelligence Reports.**Note:** This limitation applies only to Intelligence Reports.

</td><td>

True

</td></tr><tr><td>

sn\_sec\_tisc.intelligence\_report.defang\_record\_list\_urls

</td><td>

Controls whether URLs from lists will be defanged or not in intelligence reports.**Note:** This limitation applies only to Intelligence Reports.

</td><td>

False

</td></tr><tr><td>

sn\_sec\_tisc.default\_report\_email\_template

</td><td>

Sys ID of the email client template which will be used in share report in TISC workspace.This is the email template that will be used while sharing reports \(Case/Intelligence\) from TISC Workspace.

**Note:** The system property`sn_sec_tisc.reporting.email_template_sn_sec_tisc_case` is no longer supported in TISC. It has been renamed to`sn_sec_tisc.default_report_email_template`, effective with the latest release.

</td><td>

b55e22c54324021060eee0ea78b8f2df

</td></tr></tbody>
</table>