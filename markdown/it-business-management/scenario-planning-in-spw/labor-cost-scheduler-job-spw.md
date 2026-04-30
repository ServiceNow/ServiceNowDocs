---
title: Activate scheduled job to generate labor costs for your planning items
description: Activate scheduled jobs to automatically generate labor costs for attribute-based resource assignments.
locale: en-US
release: zurich
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure financials for planning items in Strategic Planning, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Activate scheduled job to generate labor costs for your planning items

Activate scheduled jobs to automatically generate labor costs for attribute-based resource assignments.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Filter the Name field to locate and open **Generate Labor Costs For Epic and other planning items**.

3.  Select **Active** and on the Scheduled Script Execution form, fill the fields.

    For a description of the field names, see [Scheduled Script Execution form to generate labor costs for planning items](../../alignment-planner-workspace/reference/gen-labor-costs-scheduled-script-execution-form-spw.md).

    **Note:** You can generate the labor costs for inactive planning items. Remove `true` in the following code line.

    `fundingEntityGr.addQuery('active', true);`

4.  Select **Update** to save your changes or **Execute Now** to run the scheduled job.


