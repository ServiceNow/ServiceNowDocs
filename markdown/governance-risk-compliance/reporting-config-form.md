---
title: Create Reporting Configuration form
description: On the Create New Reporting Configuration form, fill in the fields.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/reporting-config-form.html
release: australia
topic_type: reference
last_updated: "2026-05-12"
reading_time_minutes: 1
breadcrumb: [Create Reporting configurations, Generating Microsoft Word reports using Document designer, Manage, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Create Reporting Configuration form

On the Create New Reporting Configuration form, fill in the fields.

<table id="table_xhd_4dv_fjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Business domain

</td><td>

Domain from where the configuration is created. This field is automatically set to DRI for DRIR; references sn\_grc\_business\_domain.

</td></tr><tr><td>

Reporting item

</td><td>

Identifier for the reporting item or name of the configuration; mandatory field. The predefined record uses 'DRIR Case'. Use a short, unique label that identifies the target of the report.

</td></tr><tr><td>

Source type: Table

</td><td>

Source from which you want to fetch the data. Mandatory field; The choices are as follows: -   **Table**: Select this option when you want to import data from a table.
-   **Report**: Select this option if you want to import data from a predefined report or chart.
-   **Data visualization**: Select this option if you want to import data from a data visualization in the Performance Analytics library.

**Note:** Only list reports, pivot reports, multi-level pivot reports, horizontal and vertical bar charts, and pie charts are available for selection. Stacked bar charts and grouped bar charts are not supported.

</td></tr><tr><td>

Table

</td><td>

Source table to fetch data from. This field only appears when **Table** is selected from the **Source type** field; reference to sys\_db\_object - reference to sys\_report

</td></tr><tr><td>

Filter

</td><td>

Filter conditions to filter the records. This field only appears when **Table** is selected from the **Source type** field.

</td></tr><tr><td>

Columns

</td><td>

Column from the table whose values are to be inserted. This field only appears when **Table** is selected from the **Source type** field

</td></tr><tr><td>

Source type: Report

</td><td>

Option to select the source type as Report.

</td></tr><tr><td>

Report

</td><td>

Available report to be inserted in the report. This field only appears when **Report** is selected from the **Source type** field.

</td></tr><tr><td>

Source type: Data visualization

</td><td>

Option to select the source type as Data visualization

</td></tr><tr><td>

Data visualization

</td><td>

Data visualization option. This field only appears when **Data visualization** is selected from the **Source type** field; reference to a data-visualization record, for example. "Digital Resilience Incident Reporting Case."

</td></tr><tr><td>

Active

</td><td>

Option to indicate if the record is active. Only active records are available for selection in the document; Default=On.

</td></tr><tr><td>

Track configuration

</td><td>

Optional check box that enables change tracking for this reporting configuration. The Digital resilience incident reporting application does not use this field by default; leave it cleared unless your administrator instructs otherwise.

</td></tr></tbody>
</table>