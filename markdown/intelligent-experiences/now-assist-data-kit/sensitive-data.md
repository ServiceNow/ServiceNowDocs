---
title: Find and cleanse sensitive data
description: Scan a dataset for personally identifiable information \(PII\) and other sensitive data, and cleanse the records that the scan finds.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/now-assist-data-kit/sensitive-data.html
release: australia
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: task
last_updated: "2026-10-19"
reading_time_minutes: 1
keywords: [sensitive data, PII, scan and cleanse, Now Assist Data Kit]
breadcrumb: [Using AI Data Kit, AI Data Kit, Managing data for AI, Enable AI Experiences]
---

# Find and cleanse sensitive data

Scan a dataset for personally identifiable information \(PII\) and other sensitive data, and cleanse the records that the scan finds.

## Before you begin

The following plugins must be installed: Data Discovery \(sn\_data\_discovery\), Data Privacy \(sn\_dp\_store\_app\), and com.glide.data\_privacy.

Role required: sn\_data\_kit.admin

## About this task

New datasets are scanned automatically when they're created. If a dataset hasn't been scanned, you can scan it yourself. A dataset can be scanned only once.

The scan results appear on the dataset's Data insights tab. For details, see [View data insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-data-kit/view-data-insights.md).

## Procedure

1.  Navigate to **All** &gt; **AI Data Kit** &gt; **Home**.

2.  In the An overview of your data assets section, on the **Datasets** tab, select the dataset.

3.  On the right side of the dataset page, select the **Scan and cleanse** icon.

    The icon is in the narrow bar along the right edge of the page. Point to it to see its name.

4.  On the **Scan data** tab, check the **Scan status**.

    If the status is No scans run yet, select **Scan data**. If the dataset has already been scanned, go to the next step.

5.  Select the **Data insights** tab, and review the number of records that contain sensitive data.

6.  In the scan and cleanse panel, on the **Cleanse data** tab, select **Cleanse data**.

    **Cleanse data** is available only after a scan finds sensitive data.


## Result

The Data cleansing count on the Data insights tab shows the number of records that were cleansed.

