---
title: Find and cleanse sensitive data
description: You can scan your datasets for sensitive data, like personally identifiable information \(PII\). If you find sensitive data, then you can cleanse it from your datasets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-data-kit/sensitive-data.html
release: australia
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [Using Now Assist Data Kit, Now Assist Data Kit, Enable AI experiences]
---

# Find and cleanse sensitive data

You can scan your datasets for sensitive data, like personally identifiable information \(PII\). If you find sensitive data, then you can cleanse it from your datasets.

## Before you begin

Role required: admin

Plugins required: `sn_data_discovery`, `sn_dp_store_app` \(Data Privacy\), `com.glide.data_privacy`.

**Warning:**

The sensitive data scan has the following limitations:

-   Only structured field types stored directly in the selected table are scanned. Columns added via scripting, such as work notes or journal fields, are not evaluated.
-   The scan detects specific categories of PII such as names and email addresses using the platform vault service. It may not detect all custom or domain-specific sensitive data patterns.
-   If your dataset contains sensitive information from non-standard field types, review and manually remove that data before adding the dataset to a collection.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Data Kit** &gt; **Home**.

2.  On the **Datasets** tab, select the dataset that you want to scan for sensitive data.

3.  Select **Scan Data**.

4.  If there is sensitive data in your dataset, select **Cleanse Data** to remove it.

    You can also see the records that contain sensitive data by viewing the Data Insights tab. To learn more, see [View data insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-data-kit/view-data-insights.md).


