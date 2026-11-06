---
title: View data insights
description: View data insights to check a dataset for sensitive data or to find data quality issues in a data collection before you use it for evaluation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/now-assist-data-kit/view-data-insights.html
release: australia
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: task
last_updated: "2026-10-19"
reading_time_minutes: 1
keywords: [data insights, data quality, Now Assist Data Kit]
breadcrumb: [Using AI Data Kit, AI Data Kit, Managing data for AI, Enable AI Experiences]
---

# View data insights

View data insights to check a dataset for sensitive data or to find data quality issues in a data collection before you use it for evaluation.

## Before you begin

Role required: sn\_data\_kit.admin or sn\_data\_kit.analyst

## About this task

Datasets and data collections each have a Data insights tab, but the tab shows different information for each.

## Procedure

1.  Navigate to **All** &gt; **AI Data Kit** &gt; **Home**.

2.  In the An overview of your data assets section, select a dataset on the **Datasets** tab or a collection on the **Data collections** tab.

3.  Select the **Data insights** tab.

    |Opened from|Insight|Description|
    |-----------|-------|-----------|
    |Dataset|Data scanning|Number of records found to contain sensitive data. For details, see [Find and cleanse sensitive data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/sensitive-data.md).|
    |Data cleansing|Number of records that have been cleansed.|
    |Data collection|Data volume|Records with an unusually low character count, or significantly fewer words than the collection average. The records are listed.|
    |Missing/empty values|Fields that are null, empty, or contain placeholder values. If none are found, the section shows No issues detected.|


## What to do next

If a collection has records with low data volume or missing values, review those records in the datasets that the collection uses. To work with a smaller set of good records, [create a derived dataset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/create-derived-dataset.md).

