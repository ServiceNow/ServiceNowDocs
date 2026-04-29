---
title: Activate scheduled job to populate to multicurrency fields
description: Activate and execute the scheduled job to map your costs and work with multicurrency.
locale: en-US
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure financials for planning items Strategic Planning, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Activate scheduled job to populate to multicurrency fields

Activate and execute the scheduled job to map your costs and work with multicurrency.

## Before you begin

Role required: admin

## About this task

After upgrading from classic experience to the latest version, run this job once to populate the new investment currency fields for all existing projects. This job populate the investment currency fields for existing projects or demands from the demand currency or project currency fields, respectively.

**Note:** The multicurrency introduced a field named investment currency which is different from demand and project currency.

copies values from the corresponding demand currency, project currency, and investment objects fields to investment currency fields. This ensures that financial data aligns with the updated multicurrency model.

Once you run this job, the finanical baselines are updated with the investment currency values.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Filter the Name field to locate and open **Update multi-currency fields to investment currency for existing demands and projects**.

3.  Select **Active** and on the Scheduled Script Execution form, fill in the details.

    For a description of the field names, see [Scheduled Script Execution form to generate labor costs for planning items](../../alignment-planner-workspace/reference/gen-labor-costs-scheduled-script-execution-form-spw.md).

4.  Select **Update** to save your changes and execute the job as scheduled, or select **Execute Now** to run the scheduled job.


## What to do next

After executing the job, ensure the investment currency fields are populated correctly based on your project or demand currency.

