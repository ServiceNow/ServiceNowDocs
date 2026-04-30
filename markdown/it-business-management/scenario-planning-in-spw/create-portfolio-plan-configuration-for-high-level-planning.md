---
title: Create portfolio plan configuration for high-level planning
description: To enable high-level planning on a table that is not a planning item in Strategic Planning Workspace, create portfolio plan configuration for the table.
locale: en-US
release: zurich
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [High-level planning configuration in Strategic Planning, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Create portfolio plan configuration for high-level planning

To enable high-level planning on a table that is not a planning item in Strategic Planning Workspace, create portfolio plan configuration for the table.

## Before you begin

[Create rank configuration for high-level planning](create-rank-configuration-enable-high-level-planning.md)

Role required: admin

## About this task

After creating a global rank column and a rank configuration for that column, create a portfolio plan configuration for the table that you chose for high-level planning. Following this task, configure the Proritization and Rodmap page settings for a portfolio plan that your planning managers would create for this table.

In this task, consider the example of Strategic Priority \[sn\_gf\_strategy\] table.

## Procedure

1.  Navigate to **All** &gt; **sn\_align\_ws\_roadmap\_configuration.list**.

    A list of existing portfolio plan configuration records for the Strategic Planning tables is shown.

2.  Select **New** to create a portfolio plan configuration for your table.

3.  On the form, fill the fields.

<table id="table_d5k_mpd_cxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source table

</td><td>

Table that you want to enable high-level planning for. For example, **Strategic Priority \[sn\_gf\_strategy\]**.

</td></tr></tbody>
</table><table id="table_fj1_qkb_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Rank configuration

</td><td>

Table that is used to create the portfolio plan.The value for this field is the table selected in the **Source table** field.

</td></tr></tbody>
</table>    For complete details of the fields on this form, see [Portfolio plan configuration form](../reference/portfolio-plan-configuration-form.md).

4.  Save the form.


## What to do next

Populate global rank value for all existing records of your high-level planning table.

