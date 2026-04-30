---
title: Components installed with Export to PowerPoint for Strategic Portfolio Management
description: Several types of components are installed with activation of the Export to PowerPoint for Strategic Portfolio Management \(sn\_ppt\) add-in, including user roles and tables.
locale: en-US
release: yokohama
product: Export to PowerPoint for Application Portfolio Management
classification: export-to-powerpoint-for-application-portfolio-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference, Export to PowerPoint for Strategic Portfolio Management, Strategic Portfolio Management]
---

# Components installed with Export to PowerPoint for Strategic Portfolio Management

Several types of components are installed with activation of the Export to PowerPoint for Strategic Portfolio Management \(sn\_ppt\) add-in, including user roles and tables.

## Roles installed

<table id="table_bkk_gmk_25b"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Export to PowerPoint for Strategic Portfolio Management admin\[sn\_ppt\_export.ppt\_admin\]

</td><td>

-   Create, edit, and manage the attributes required to generate Microsoft PowerPoint templates.
-   Assign this role in confidence because it is a high security role for the Export to PowerPoint application with access to modify the source code for Scripted Elements.

</td><td>

sn\_ppt\_export.ppt\_user

</td></tr><tr><td>

Export to PowerPoint for Strategic Portfolio Management user\[sn\_ppt\_export.ppt\_user\]

</td><td>

-   Create a template, upload it to the ServiceNow instance, generate, and download the project status report.
-   By default, users with the project\_user role are assigned this role.

</td><td>

None

</td></tr></tbody>
</table>## Tables installed

<table id="table_yn4_dnm_m5b"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

PowerPoint Cell Formatter\[sn\_ppt\_export\_ppt\_cell\_formatter\]

</td><td>

Stores the color properties for text, text background, table cell, and shape fill.

</td></tr><tr><td>

PowerPoint Element\[sn\_ppt\_export\_ppt\_element\]

</td><td>

Stores the required elements to generate aMicrosoft PowerPoint template.

</td></tr><tr><td>

PowerPoint Formatter\[sn\_ppt\_export\_ppt\_formatter\]

</td><td>

Stores the text formatting options.

</td></tr><tr><td>

PowerPoint Formatter Mapping\[sn\_ppt\_export\_ppt\_formatter\_mapping\]

</td><td>

Stores the format mapping for the tokens.

</td></tr><tr><td>

PowerPoint Report Type\[sn\_ppt\_export\_ppt\_report\_type\]

</td><td>

Stores report types that can be used to generate a report.

</td></tr><tr><td>

PowerPoint Template\[sn\_ppt\_export\_ppt\_template\]

</td><td>

Stores the metadata required for the templates.

</td></tr><tr><td>

PPT Service Request Log\[sn\_ppt\_export\_ppt\_poi\_service\_request\_log\]

</td><td>

Stores service requests logs.

</td></tr><tr><td>

Related Table\[sn\_ppt\_export\_ppt\_related\_table\]

</td><td>

Stores related tables for a report.

</td></tr><tr><td>

Scripted Element\[sn\_ppt\_export\_ppt\_scripted\_element\]

</td><td>

Stores the supported chart types, such as line chart and bar chart.

</td></tr></tbody>
</table>|Template name|Description and use case|Data included|
|-------------|------------------------|-------------|
|Project Report Template - Default|A comprehensive project report template designed for detailed project reviews. Use this template for in-depth project status meetings with project teams and stakeholders.|Project details, task breakdown, milestone status, resource allocations|
|Project Status Report Template - default|A concise executive summary template designed for high-level status updates. Use this template for portfolio reviews, steering committee meetings, and executive dashboards.|Project overview, key metrics, status indicators, high-level timeline|

**Tip:**

To view and manage all available templates, navigate to **All** &gt; **PowerPoint Management** &gt; **PowerPoint Templates**.

**Parent Topic:**[Export to PowerPoint Reference](export-ppt-reference.md)

