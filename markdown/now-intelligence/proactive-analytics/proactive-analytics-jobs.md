---
title: Proactive analytics jobs
description: Proactive analytics insights are activated and generated through several jobs on the Sys Jobs \[sys\_job\] table. All jobs run daily, at times set in Schedule Item \[sys\_trigger\] records.
locale: en-US
release: yokohama
product: Proactive Analytics
classification: proactive-analytics
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Proactive analytics insights on dashboards, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Proactive analytics jobs

Proactive analytics insights are activated and generated through several jobs on the Sys Jobs \[sys\_job\] table. All jobs run daily, at times set in Schedule Item \[sys\_trigger\] records.

<table id="table_fzm_s3k_fcc"><thead><tr><th>

Name

</th><th>

Java class

</th><th>

Job details

</th><th>

Scheduled item \[sys\_trigger\]

</th></tr></thead><tbody><tr><td>

KPI Signals Analytics Job

</td><td>

com.snc.pa.job.SignalsAnalyticsJob

</td><td>

Converts active signals to insights and/or proactive analytics flow trigger events.

</td><td>

KPI Signals Analytics Job

</td></tr><tr><td>

PA Forecast Job

</td><td>

com.snc.pa.forecast.PAForecastJob

</td><td>

Checks targets per UUID against the forecast and generates any triggered notifications.

</td><td>

PA Forecast Job Schedule

</td></tr><tr><td>

PATarget

</td><td>

com.snc.pa.job.PATargetCheckJob

</td><td>

Fires a target notification summary event.

</td><td>

Check PA Targets

</td></tr><tr><td>

PAThreshold

</td><td>

com.snc.pa.job.PAThresholdCheckJob

</td><td>

Fires a threshold reached event for each threshold whose condition is satisfied.

</td><td>

Check PA Thresholds

</td></tr><tr><td>

Trend Insights Job

</td><td>

com.snc.pa.job.TrendAnalyticsJob

</td><td>

Analyzes indicator trends daily, flagging significant deviations within the last 30 days.

</td><td>

Trend Insights Job Schedule

</td></tr><tr><td>

TriggerDefinitionProactiveAnalytics

</td><td>

com.snc.pa.job.TriggerDefinitionProactiveAnalyticsJob

</td><td>

Checks for the existence of a Performance Analytics Premium plugin, and if one is present, activates the Proactive Analytics trigger definition in sys\_hub\_trigger\_definition.

</td><td>

Proactive Analytics Trigger Definition Activation Job

</td></tr></tbody>
</table>