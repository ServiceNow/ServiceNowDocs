---
title: Execute the Temperature Beyond Threshold MetricBase trigger
description: Monitor temperature thresholds using the Temperature Beyond Threshold MetricBase trigger, which reads the time-series data from the Occupancy and Environment Data MetricBase data and initiates Workflow Studio flows. This MetricBase Trigger sends the email notification to the concerned person or group when the temperature in a space exceeds the defined threshold.
locale: en-US
release: yokohama
product: Workplace Connectors
classification: workplace-connectors
topic_type: task
last_updated: "2025-03-26"
reading_time_minutes: 1
breadcrumb: [Configure, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Execute the Temperature Beyond Threshold MetricBase trigger

Monitor temperature thresholds using the Temperature Beyond Threshold MetricBase trigger, which reads the time-series data from the Occupancy and Environment Data MetricBase data and initiates Workflow Studio flows. This MetricBase Trigger sends the email notification to the concerned person or group when the temperature in a space exceeds the defined threshold.

## Before you begin

**Note:** The application comes with seed data or pre-filled values for the Temperature Beyond Threshold trigger. For more information about MetricBase triggers, see [Triggering flows using MetricBase data](https://www.servicenow.com/docs/access?context=metricbase-triggers&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **MetricBase** &gt; **MetricBase Triggers** &gt; **Trigger Definitions**.

2.  Select **Temperature Beyond Threshold**.

3.  On the form, review and update the field details.

<table id="table_dc3_kqd_52c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Aggregator

</td><td>

Option to select the retention policy aggregator. Select from the following options:-   Max
-   Min
-   Average


</td></tr><tr><td>

Window

</td><td>

The aggregate duration to check temperature for a space. For example, 30 minutes.

</td></tr></tbody>
</table>4.  Select **Update**.


**Parent Topic:**[Configure Workplace Connectors](../concept/configure-workplace-connectors.md)

**Previous topic:**[Extension point definition for Wi-Fi data](wsd-extension-point-definition-for-wifi-data.md)

**Next topic:**[Workplace Connectors references](../concept/workplace-connectors-references.md)

