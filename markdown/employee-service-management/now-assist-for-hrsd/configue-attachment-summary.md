---
title: Configure attachment summary
description: Customize the case summarization skill in ServiceNow Otto for HRSD to include summaries of case attachments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/now-assist-for-hrsd/configue-attachment-summary.html
release: zurich
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, ServiceNow Otto for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Configure attachment summary

Customize the case summarization skill in ServiceNow Otto for HRSD to include summaries of case attachments.

## Before you begin

Role required: sn\_hr\_core.admin

## Procedure

1.  Navigate to **All****&gt;ServiceNow Otto Admin****&gt;Skills**.

2.  Select **Employee**, then select **HRSD**.

3.  Make a copy of the case summarization skill.

    For more information, see [Make a copy of AI skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/make-a-copy-of-a-now-assist-skill.md).

4.  Navigate to the Choose input step.

5.  In the **+New data source** drop-down, select **Activity: Attachment**.

    Configure this data source for all required input templates \(Case new, Case work in progress, or Case resolved states\).

6.  Review the remaining sections, then select **Activate**.


**Parent Topic:**[Configure ServiceNow Otto for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/now-assist-for-hrsd/configure-now-assist-hr.md)

