---
title: Run a scheduled job to update the TCO score range
description: Run the Update Score Range in Indicator Score Table scheduled job to populate the Total Cost of Ownership \(TCO\) score range on existing Indicator Score \(apm\_app\_indicator\_score\) records when the Score range field is not populated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-run-job-update-score-range-indicator-score.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [TCO score range, indicator score, scheduled job, portfolio TCO]
breadcrumb: [Configure application total cost of ownership \(TCO\) in Enterprise Architecture Workspace, Configure EA Workspace using the Setup page, Configuring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Run a scheduled job to update the TCO score range

Run the **Update Score Range in Indicator Score Table** scheduled job to populate the Total Cost of Ownership \(TCO\) score range on existing **Indicator Score** \(apm\_app\_indicator\_score\) records when the **Score range** field is not populated.

## Before you begin

Role required: admin

## About this task

The **Business applications by TCO score** widget on the **Portfolio TCO** tab of the Dashboard page reads the TCO score band directly from a **Score range** field on the **Indicator Score** \(apm\_app\_indicator\_score\) table.

If you're upgrading from a previous release, your existing **Indicator Score** records don't have this field populated. The widget shows empty state as the X-axis label instead of the TCO score bands. New installations aren't affected because the field is populated automatically as indicator scores are generated.

To populate the **Score range** field on existing records, run the **Update Score Range in Indicator Score Table** scheduled job. This is a one-time, on-demand job that is inactive by default.

**Note:** The time the job takes to run depends on the number of records in the **Indicator Score** \(apm\_app\_indicator\_score\) table.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  In the Name field, enter `Update Score Range in Indicator Score Table` and press Enter to filter the list.

3.  Open the **Update Score Range in Indicator Score Table** scheduled job.

4.  Verify that your application scope is set to Enterprise Architecture Workspace.

    For information on changing the application scope, see [Application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/c_ApplicationPicker.md).

5.  Select the **Active** check box to activate the job.

6.  Select **Execute Now**.


## Result

The **Score range** field is populated on your existing **Indicator Score** records, and the **Business applications by TCO score** widget displays the TCO score bands.

**Parent Topic:**[Configure application total cost of ownership \(TCO\) in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-setup-app-tco.md)

**Related topics**  


[Exploring total cost of ownership \(TCO\) in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-manage-application-tco.md)

[Manage application total cost of ownership \(TCO\) in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-app-tco.md)

[Set the fiscal period property for TCO dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-set-property-tco-dashboards.md)

[Application indicator score calculation in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-application-indicator-score-calculation.md)

