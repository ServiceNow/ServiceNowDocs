---
title: ITSM Virtual Agent Analytics reference
description: Reference information for scheduled jobs that collect ITSM Virtual Agent analytics data and scripts that configure topic clustering.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-va-analytics-reference.html
release: zurich
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: reference
last_updated: "2026-07-01"
reading_time_minutes: 1
keywords: [Now Assist, agentic AI, generative AI, Gen AI]
breadcrumb: [Use ITSM Virtual Agent analytics dashboard, ServiceNow Otto for IT Service Management \(ITSM\), IT Service Management]
---

# ITSM Virtual Agent Analytics reference

Reference information for scheduled jobs that collect ITSM Virtual Agent analytics data and scripts that configure topic clustering.

## ITSM Virtual Agent data collection jobs

Run scheduled jobs to retrieve data.

To access the jobs, navigate to **All** &gt; **System Definition** &gt; **Scheduled jobs**.

-   The **\[Historical\] - ITSM Conversational Analytics** scheduled job runs on-demand. Run this job to retrieve historical data for the last six months.
-   The **\[Daily\] - ITSM Conversational Analytics** scheduled job retrieves daily data. This job automatically runs at midnight everyday.

## ITSM Virtual Agent analytics GAF clustering

To configure the Group Action Framework \(GAF\) to cluster topics and use chat summarization to create topic names, run the **Activate topic clustering for Now Assist ITSM dashboard** script. [Configure Group Action Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configure-gaf.md)\[Omitted image "now-assist-itsm-script-execution-va-dashboard.png"\] Alt text: Now Assist for ITSM scheduled script execution

