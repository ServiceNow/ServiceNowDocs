---
title: Activate scheduled jobs to generate labor costs for your planning items
description: Activate scheduled jobs to automatically generate labor costs for attribute-based resource assignments.
locale: en-US
release: yokohama
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure financials for planning items in Strategic Planning, Configure, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Activate scheduled jobs to generate labor costs for your planning items

Activate scheduled jobs to automatically generate labor costs for attribute-based resource assignments.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Filter the Name field to locate and open **Generate labor costs for demands and projects** and **Generate Labor Costs For Epic** jobs.

3.  Select **Active** and on the Scheduled Script Execution form, fill the fields.

    For a description of the field names, see [Scheduled Script Execution form to generate labor costs for planning items](../../alignment-planner-workspace/reference/gen-labor-costs-scheduled-script-execution-form-spw.md).

    **Note:** You can generate the labor costs for inactive planning items. Remove `true` from the following code lines for the respective planning items to include the inactive planning items.

    -   Epics: `epicGr.addQuery("active", true);`
    -   Projects: `projectsGr.addQuery("active", true)`
    -   Demands: `demandGr.addQuery("active", true);`
4.  Select **Update** to save your changes or **Execute Now** to run the scheduled job.


