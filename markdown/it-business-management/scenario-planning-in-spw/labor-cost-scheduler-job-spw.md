---
title: Scheduled job to generate labor costs
description: Activate scheduled jobs to automatically generate labor costs for attribute-based resource assignments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/scenario-planning-in-spw/labor-cost-scheduler-job-spw.html
release: brazil
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure financials for planning items Strategic Planning, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Scheduled job to generate labor costs

Activate scheduled jobs to automatically generate labor costs for attribute-based resource assignments.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Filter the Name field to locate and open **Generate Labor Costs For Epic and other planning items**.

3.  Select **Active**.

4.  On the Scheduled Script Execution form, fill the fields.

    For a description of the field names, see [Scheduled Script Execution form to generate labor costs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/scenario-planning-in-spw/gen-labor-costs-scheduled-script-execution-form-spw.md).

    **Note:** You can generate the labor costs for inactive planning items. Remove `true` in the following code line.

    `fundingEntityGr.addQuery('active', true);`

5.  Select **Update** to save your changes or **Execute Now** to run the scheduled job.


