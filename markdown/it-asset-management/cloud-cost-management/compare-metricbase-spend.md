---
title: Compare MetricBase data with spend data
description: Compare MetricBase \(Clotho\) data with your Spend data for Amazon Web Services \(AWS\), Microsoft Azure, and Google Cloud Platform \(GCP\) to diagnose and troubleshoot Cloud Cost Management billing issues.
locale: en-US
release: zurich
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Cloud Cost Management, IT Asset Management]
---

# Compare MetricBase data with spend data

Compare MetricBase \(Clotho\) data with your Spend data for Amazon Web Services \(AWS\), Microsoft Azure, and Google Cloud Platform \(GCP\) to diagnose and troubleshoot Cloud Cost Management billing issues.

## Before you begin

Role required: Cloud Insights Admin \[sn\_clin\_core.insights\_admin\]

Request the MetricBase \[com.snc.clotho\] plugin. For more information, see [Requesting the MetricBase product](https://www.servicenow.com/docs/access?context=request-metricbase&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

Verify that the Billing Download job has been completed successfully for the cloud provider.

## About this task

**Important:** This feature is available with the Cloud Cost Management 8.0.0 version or later.

## Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Tools**.

2.  Select **Compare MetricBase with spend data**.

3.  On the form, fill in the fields.

<table id="table_iml_mll_cbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Provider

</td><td>

Cloud provider for which you want to compare MetricBase \(Clotho\) data with your Spend data.-   AWS
-   Azure
-   GCP


</td></tr><tr><td>

Cost type

</td><td>

Contractual payment agreement with the provider.-   Actual: Each billing period, your organization pays for direct cloud services.
-   Amortized: Your organization pays the effective cost of the upfront and monthly reservation fees spread across the billing period. The amortized cost type is described in detail on the provider's site.


</td></tr><tr><td>

Billing month

</td><td>

Months for which billing data is available based on the provider you select.This field is populated only with those months for which billing data is available.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

A request with a unique number gets created and a CSV file is attached to the request item, which lists the comparison data. The process to generate the CSV file runs in the background and the file is attached to the request item when the processing is complete.

If there are any errors, the **Work notes** field of this request item is updated and Cloud Cost Management doesn't generate the CSV file.

## What to do next

Select the **Requested Items** tab and then select the Requested Items number to navigate to the CSV file. In the Attachments section, you can find the CSV file. Download this file to analyze any mismatch in the cost values from both of the sources. You can also filter the data according to your requirements.

**Parent Topic:**[Using Cloud Cost Management](../concept/using-cloud-insights.md)

