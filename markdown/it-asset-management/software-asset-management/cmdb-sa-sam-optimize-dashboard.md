---
title: Manage SAM advisor scope in CMDB success advisor
description: Manage the scope of your advisor for Software Asset Management \(SAM\) by editing the software products in CMDB success advisor to support your targeted SAM outcomes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-asset-management/software-asset-management/cmdb-sa-sam-optimize-dashboard.html
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-07-22"
reading_time_minutes: 1
keywords: [manage SAM advisor scope, edit dashboard scope, SAM software product selection]
breadcrumb: [Set up advisor, Use SAM advisor, Software Asset Management, IT Asset Management]
---

# Manage SAM advisor scope in CMDB success advisor

Manage the scope of your advisor for Software Asset Management \(SAM\) by editing the software products in CMDB success advisor to support your targeted SAM outcomes.

## Before you begin

Role required: sam\_admin or sn\_cmdb\_admin

## About this task

Control which software products are included in the SAM advisor dashboard in CMDB success advisor. Add or remove individual software products, or select every product for a publisher at once.

## Procedure

1.  On the SAM advisor dashboard, select **Edit dashboard scope**.

2.  Review your previously selected software products, shown as already selected in the Edit dashboard scope dialog box.

    Add or remove software products using the same actions described in [Get started with CMDB success advisor setup for SAM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/software-asset-management/cmdb-sa-sam-get-started.md).

3.  Select **Save** to apply the changes.

    **Note:** If you save without making any changes to the selection, no confirmation message appears.


## Result

The SAM dashboard in CMDB success advisor is updated to reflect the data based on the software product selection. A confirmation message summarizes the software products added or removed. Dashboard metrics refresh once daily when the **CMDB Advisor - SAM Daily Data Collection** scheduled job runs. The scheduled job invokes the **CMDB success advisor data collection for SAM** Performance Analytics job to recalculate the pre-aggregated indicators used throughout the dashboard. For more information about Performance Analytics jobs, see [Collecting indicator scores](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/c_ClctData.md). Changes to your software product selection appear in the dashboard metrics after this job's next run, not immediately. For the full list of CMDB success advisor scheduled jobs, see [Components installed with CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/cmdb-sa-components-installed.md).

