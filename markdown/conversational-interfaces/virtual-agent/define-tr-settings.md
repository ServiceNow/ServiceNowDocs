---
title: Configure analysis reports for Topic Recommendations
description: To generate Topic Recommendations, specify a default data source \(ServiceNow table and field\) and the conditions for filtering the data records.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Virtual Agent Topic Recommendations, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Configure analysis reports for Topic Recommendations

To generate Topic Recommendations, specify a default data source \(ServiceNow table and field\) and the conditions for filtering the data records.

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

When configuring analysis reports, consider the following:

-   You can define only one setting per data table and taxonomy pair.
-   Two data sets for the ITSM taxonomy \(Incident and Requests\) are provided by default, but you can define your own data sources.
-   In the Australia release, Topic Recommendations requires a minimum of 10,000 records in your analysis scope \(data source\). This minimum provides a reasonably sized data set to achieve a certain level of quality in the analyses.
-   Keep your analysis scope \(data source\) under 300,000 records. In the Australia release, this is the maximum number allowed. This limit maximizes the performance of the analysis report.
-   You can schedule analysis reports to run automatically at specified intervals.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  Select **Virtual Agent**.

3.  Under Topic Recommendations, click **View all**.

4.  Select **New**.

5.  On the form, fill in the fields.

    For details, see [Topic Recommendations settings](../reference/tr-settings-page.md).

6.  Select **Save**.


## Result

The data source that you defined for a given table and taxonomy displays as a section on the Topic Recommendations page. You can now [run a topic recommendation analysis](run-tr-analysis.md).

