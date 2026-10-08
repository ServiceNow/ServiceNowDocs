---
title: Create a report on IGT question results
description: Create a report that shows the answers to IGT questions together with the functional location, equipment, standard, and shift of each task.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/industrial-connected-workforce/digital-factory-workspace/create-report-igt-question-results.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: task
last_updated: "2026-09-25"
reading_time_minutes: 1
keywords: [Industrial Guided Tasks, question results, create report]
breadcrumb: [Industrial Guided Tasks, Use, Digital Factory Workspace, Industrial Connected Workforce]
---

# Create a report on IGT question results

Create a report that shows the answers to IGT questions together with the functional location, equipment, standard, and shift of each task.

## Before you begin

Role required: sn\_icw.report\_user

## About this task

Reports on IGT question results use the Industrial Guided Task Result \[sn\_icw\_igt\_results\] database view as their source. For the fields available in the view, see [Industrial Guided Task Result database view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/igt-results-database-view.md).

## Procedure

1.  Create a report.

    For more information about creating reports, see [Report types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/report-types-creation-details-rd.md).

2.  On the **Data** tab, enter a name for the report.

3.  In the **Source type** field, select **Table**.

4.  In the **Table** field, select **Industrial Guided Task Result \[sn\_icw\_igt\_results\]**.

5.  Select **Next** and select a report type.

6.  Configure the report.

    To focus on specific inspection results, filter or group by operational context fields, such as **Functional location**, **Equipment**, **Standard**, or **Planned start shift**. To report on a single question, filter on **Assessment question**.

7.  Select **Save**.


**Parent Topic:**[Using Industrial Guided Tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/using-industrial-guided-tasks.md)

