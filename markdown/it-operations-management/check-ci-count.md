---
title: Check CI count used for ITOM subscriptions
description: View daily CI counts or the average of the last 90 daily counts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/check-ci-count.html
release: australia
product: IT Operations Management
classification: it-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using ITOM/OT SU Licensing, ITOM/OT SU Licensing and subscriptions, IT Operations Management]
---

# Check CI count used for ITOM subscriptions

View daily CI counts or the average of the last 90 daily counts.

## Before you begin

Ensure that your organization has purchased ITOM subscriptions. You cannot view the information in the **ITOM License** module without subscriptions.

Role required: sn\_itom\_license.reader

## About this task

ITOM applications, such as ITOM Visibility, ITOM Discovery, ITOM AIOps, Health Log Analytics, ITOM Cloud Accelerate, and ITOM Optimization provide information on the resources they handle. These resources, called configuration items \(CIs\), are what ITOM applications find, monitor, and store in the CMDB. The ITOM/OT SU Licensing module combines this CI data with the subscription information of your organization to produce statistics on the subscription usage and consumption of the ITOM applications. For more information about the licensing workflow process, see [Data collection and aggregation for licensing process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/data-collection-aggregation-licensing-process.md).

This information does not include any statistics on subscriptions purchased in bundles. For complete information on subscriptions, [view subscription statistics for IT Operations Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/view-itom-license-statistics.md).

## Procedure

1.  Navigate to **ITOM License** &gt; **License Report**.

    \[Omitted image "itom-license-report.png"\] Alt text: The License Report window showing subscription statistics for the IT Operations Management applications a la carte.

    To know more about the fields in the Licence Report window, see [License Report form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/license-report-form.md).

2.  In the **Total Count** column, view the average daily CI counts for the last 90 days.

3.  View the daily CI count in one of the following ways.

    -   Set the **Aggregated** filter condition to **\[Aggregated\] \[is\] \[false\]** and select **Run**.
    -   Navigate to **ITOM License** &gt; **License Daily Usage Count**.

