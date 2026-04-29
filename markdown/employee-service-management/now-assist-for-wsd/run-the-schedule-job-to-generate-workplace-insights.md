---
title: Run the scheduled job to generate workplace insights
description: Run the Generate Workplace Insights - Weekly scheduled job to generate workplace insights based on the configured data source and prompt configuration.
locale: en-US
release: australia
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: task
last_updated: "2025-10-27"
reading_time_minutes: 1
breadcrumb: [Insight cards on the Workplace Central dashboard, Workplace Advisor Overview, Using AI agent workflows in Now Assist for WSD, Now Assist for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Run the scheduled job to generate workplace insights

Run the **Generate Workplace Insights - Weekly** scheduled job to generate workplace insights based on the configured data source and prompt configuration.

## Before you begin

Role required: admin

## About this task

When the scheduled job is run, it creates multiple executions in the AI Config Executions table.

The execution process involves:

-   Generating insight executions for each data source
-   Sending data and prompts to the large language model \(LLM\) asynchronously
-   Mapping returned insights to users and storing them for display on the Workplace Insights dashboard

**Note:** By default, the scheduled job is set to run weekly on the specified time. You can also run the scheduled job based on your preferences.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Job**.

2.  From the Scheduled Jobs list, select **Generate Workplace Insights - Weekly**.

3.  Run the job by selecting **Execute Now**.


**Parent Topic:**[Insight cards on the Workplace Central dashboard](../concept/insight-cards-on-the-workplace-central-dashboard.md)

