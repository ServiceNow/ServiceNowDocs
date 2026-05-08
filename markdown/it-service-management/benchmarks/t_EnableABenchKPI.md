---
title: Configure KPI participation
description: Review and configure Benchmarks KPI participation by opting in or out of categorized KPIs.
locale: en-US
release: australia
product: Benchmarks
classification: benchmarks
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Benchmark KPIs, Benchmarks, IT Service Management]
---

# Configure KPI participation

Review and configure Benchmarks KPI participation by opting in or out of categorized KPIs.

## Before you begin

Role required: sn\_bm\_client.benchmark\_admin

## Procedure

1.  Opt in for Benchmarks.

    For more information, see [Enable Benchmarks](t_EnableBench.md).

2.  On the Benchmarks configuration page, view the KPI categories in the KPI participation section.

3.  Select a category for which you want to view KPI details and select **Review and configure**.

    On the respective category page, a summary of KPIs, current participation status, descriptions, formulas for KPI calculation, and conditions for contributing indicators are displayed.

4.  Opt in for KPI participation.

    1.  Select the vertical ellipsis next to the KPI that you want to opt in to.

    2.  Select **Opt in**.

5.  Opt out of KPI participation.

    1.  Select the vertical ellipsis next to the KPI that you want to opt out of.

    2.  Select **Opt out**.

6.  Modify KPI details.

    1.  Select the vertical ellipsis next to the KPI that you want to modify.

    2.  Select **Modify**.

    3.  Modify KPI details such as the description, formula for KPI calculation, and conditions for contributing indicators.

7.  Create or schedule a Benchmarks historical data collection job for a newly enabled KPI.

    For information about how to create or schedule a data collection job, see Create or schedule a data collection job. The recommended time interval to collect data for a new KPI is 60 days.

8.  Execute the Benchmarks historical data collection job to collect data for the new KPI.

    1.  Navigate to **Platform Analytics** &gt; **Data Collector** &gt; **Jobs**.

    2.  Find and open the historical data collection job that you created.

    3.  Select **Execute**.

        The collected data scores are stored in the Platform Analytics Score \(pa\_scores\) table.

9.  Upload the collected data to the centralized Benchmarks instance.

    1.  In the Benchmarks historical data collection job, navigate to the **Job Logs** related list.

    2.  Make sure that the state for the historical data collection job is **Collected**.

        This state indicates that the job is complete and all data for the set period is collected.

    3.  Navigate to **System Definition** &gt; **Scheduled Jobs**.

    4.  Find and open the **Copy historical scores from PA to Benchmarks table** job.

    5.  Select **Execute Now**.

10. Download the Benchmarks scores manually to your instance to view the scores before they are automatically downloaded.

    1.  Navigate to **System Definition** &gt; **Scheduled Jobs**.

    2.  Find and open the **Download the benchmark scores** job.

    3.  Select **Execute Now**.


-   **[Configure resolved incident Benchmarks KPIs](t_ConfigResIncBenchKPIs.md)**  
The source for the KPIs containing resolved incident data is the **resolved\_at** field in the Incident \[incident\] table, which may not exist in some environments. In this case, additional configuration is required to use these KPIs.

**Parent Topic:**[Benchmark KPIs](../concept/c_BenchKPIConfig.md)

