---
title: Related Tables form
description: Use the Related Tables form to define the child tables for the configured parent table. This Related Tables helps in fetching data to export the project status report as Microsoft PowerPoint.
locale: en-US
release: zurich
product: Export to PowerPoint for Application Portfolio Management
classification: export-to-powerpoint-for-application-portfolio-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Export to PowerPoint for Strategic Portfolio Management, Strategic Portfolio Management]
---

# Related Tables form

Use the Related Tables form to define the child tables for the configured parent table. This Related Tables helps in fetching data to export the project status report as Microsoft PowerPoint.

<table id="table_fbp_2d5_c5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the child table to include in the export.

</td></tr><tr><td>

Parent relation column

</td><td>

The column that defines the relationship between the parent and child tables. This field determines how the child table data is joined to the parent record.For more information on how to manage Related Tables, see [Manage Related Tables and Scripted Elements forms](../task/manage-components-export-ppt.md).

</td></tr><tr><td>

Enable custom script

</td><td>

Select this option to enable custom scripting for the related table data. When enabled, you can write server-side JavaScript to customize how child table data is fetched, filtered, or transformed before it is included in the PowerPoint export.**Important:** Custom scripts run with the permissions of the current user. Test scripts thoroughly on a non-production instance before deploying to production.

</td></tr><tr><td>

Advanced

</td><td>

Expand this section to access advanced configuration options for controlling how the related table data is rendered in the PowerPoint export, including field mappings, sort order, and display formatting.

</td></tr></tbody>
</table>**Parent Topic:**[Export to PowerPoint Reference](export-ppt-reference.md)

