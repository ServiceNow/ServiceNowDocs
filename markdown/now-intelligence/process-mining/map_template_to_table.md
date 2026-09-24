---
title: Map a template to a table
description: Map a template to a table so that launching Process Mining from a Performance Analytics indicator or a list view from any workspace uses the right template.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/process-mining/map\_template\_to\_table.html
release: brazil
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [process mining, template mapping, connected experiences]
breadcrumb: [Process Mining templates, Use, Process Mining, Platform Analytics]
---

# Map a template to a table

Map a template to a table so that launching Process Mining from a Performance Analytics indicator or a list view from any workspace uses the right template.

## Before you begin

Role required: sn\_process\_mining\_power\_user or higher.

Analysts and users without a Process Mining role can't see the Template mapping page.

## About this task

Only Standard templates can be selected for a mapping.

**Note:** Template mappings are domain separated.

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

2.  From the Process Mining projects page, select the gear icon, then select **Manage project templates**.

    \[Omitted image "man-temp.png"\] Alt text: Manage project templates button

3.  Select the **Template mapping** tab on the Manage project templates page.

    \[Omitted image "temp-mapping.png"\] Alt text: Template mapping tab

4.  Select **New**.

5.  Fill in the fields.

<table id="table_template_mapping_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Determines where users can initiate Process Mining using this mapping. Two values are allowed:

-   Default: For Performance Analytics indicator
-   List: For list view


</td></tr><tr><td>

Table

</td><td>

The table this mapping applies to.

</td></tr><tr><td>

Template

</td><td>

The Standard template to use. Only templates based on the selected table appear in this list.

</td></tr></tbody>
</table>6.  Select **Save**.

    **Note:** If a mapping already exists for the same type and table, you get an error and the new mapping isn't created.


## Result

A template mapping is available.

**Parent Topic:**[Process Mining templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/pm_templates.md)

