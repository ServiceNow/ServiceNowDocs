---
title: Troubleshooting Benchmarks errors
description: Troubleshoot and resolve common errors when setting up or running Benchmarks.
locale: en-US
release: zurich
product: Benchmarks
classification: benchmarks
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Benchmarks, IT Service Management]
---

# Troubleshooting Benchmarks errors

Troubleshoot and resolve common errors when setting up or running Benchmarks.

<table id="table_yrc_45y_xy"><thead><tr><th>

Scenario

</th><th>

Reason

</th><th>

Action

</th></tr></thead><tbody><tr><td>

No data in dashboard after opting in.

</td><td>

The download REST API for six months failed or there is a connection failure.

</td><td>

Verify in the sysevent table that the sn\_bm\_client.download.scores.6months event is processed.

</td></tr><tr><td>

No instance data is shown in the dashboard for the last month.

</td><td>

PA data collection or scorecards API failure.

</td><td>

-   Make sure the condition in the indicator source, script field in the indicator, and additional conditions in the indicator are correct.
-   Verify that historical data of the last month for the KPI is collected.
    1.  Navigate to **Platform Analytics** &gt; **Data Collector** &gt; **Jobs**.
    2.  Find and open the historical data collection job for the KPI.
    3.  Navigate to the **Job Logs** related list.
    4.  Make sure that the state for the historical data collection job is **Collected**.

</td></tr><tr><td>

No global or cohort benchmark scores in dashboard for the last month.

</td><td>

-   The download REST API failed or there is a connection failure.
-   The minimum data required to generate global or cohort scores for a KPI isn't available due to insufficient customer participation in a cohort or peer group segment.

</td><td>

-   Verify in the sysevent table that the sn\_bm\_client.download.scores event is processed.
-   Make sure that each cohort has a minimum of 10 participating customers.

</td></tr><tr><td>

Opt-in process fails.

</td><td>

Authentication failed or the instance type is not supported.

</td><td>

Contact Customer Service and Support team.

</td></tr><tr><td>

Incorrect or no KPI data in the Benchmarks dashboard.

</td><td>

-   KPI condition configuration
-   The minimum historical data scores for KPIs are not available.

</td><td>

-   Verify the KPI definition and conditions in **Performance Analytics** &gt; **Sources** &gt; **Indicator Sources**.
-   Make sure that a minimum of one to two months of aggregate monthly historical data for a KPI is available. The recommended time interval is 60 days.

</td></tr><tr><td>

No data in Percentile Rank list view.

</td><td>

Percentile Rank shows N/A due to the following reasons.-   You are viewing an industry that you are not a part of.
-   The minimum data required to generate global or cohort scores for a KPI isn't available due to insufficient customer participation in a cohort or peer group segment.

</td><td>

-   View the industry in which your scores are included.
-   Make sure that each cohort has a minimum of 10 participating customers.

</td></tr><tr><td>

No data in Top Performer score.

</td><td>

Top Performer score shows N/A if the minimum historical data scores for KPIs are not available.

</td><td>

Make sure that a minimum of one to two months of aggregate monthly historical data for a KPI is available. The recommended time interval is 60 days.

</td></tr></tbody>
</table>