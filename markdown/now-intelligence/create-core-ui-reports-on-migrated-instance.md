---
title: Create Core UI reports on an upgraded instance
description: On upgraded instances, including ones fully migrated to Platform Analytics, you can create Core UI reports from the Platform Analytics Data visualizations library.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/create-core-ui-reports-on-migrated-instance.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Create Core UI reports on an upgraded instance

On upgraded instances, including ones fully migrated to Platform Analytics, you can create Core UI reports from the Platform Analytics Data visualizations library.

## Before you begin

A ServiceNow AI Platform administrator should create the **com.snc.par.coreui.report\_create.enabled** property and set it to `true`. Otherwise, only report\_admin users or higher can create Core UI reports, and only directly in the Reports \[sys\_report\] table.

Role required: If the **com.snc.par.coreui.report\_create.enabled** system property is `true`, any user with an internal role can create reports.

## About this task

**Important:** You cannot create Core UI reports on instances that were net new on Xanadu or later. On instances that were net new on older releases, you can continue to create Core UI reports, even if the instance was fully migrated to Platform Analytics.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data visualizations**

2.  Select **Create data visualization**.

3.  In the New data visualization modal, select **Core UI** and then select **Create data visualization**.

    \[Omitted image "create-core-ui-dv-from-library.png"\] Alt text: Create new Core UI data visualization on a migrated instance

    The Report Designer opens.

4.  Follow the instructions in the topic [Create a report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/reporting/t_CreateYourOwnReport.md) to create your report.


**Parent Topic:**[Creating data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/creating-data-visualizations.md)

