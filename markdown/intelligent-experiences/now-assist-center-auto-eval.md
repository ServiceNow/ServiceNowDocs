---
title: AI Admin Center Auto Eval dashboard
description: Use the AI Admin Center Auto Eval dashboard to monitor evaluation coverage and benchmark results for your AI assets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-center-auto-eval.html
release: australia
topic_type: concept
last_updated: "2026-07-31"
reading_time_minutes: 2
keywords: [AI Admin Center, Now Assist Center, AI, AI setup, auto evaluation]
breadcrumb: [View AI assets usage and performance, Monitor, AI Admin Center, Enable AI experiences]
---

# AI Admin Center Auto Eval dashboard

Use the AI Admin Center Auto Eval dashboard to monitor evaluation coverage and benchmark results for your AI assets.

## AI Admin Center Auto Eval dashboard

The AI Admin Center Auto Eval dashboard displays a summary of evaluation activity and a list of AI assets with their evaluation status and benchmark results.

Use the **Date** and **Asset Type** filters at the top of the dashboard to refine the data displayed.

**Important:** Select a date range of 7 days or fewer. Evaluation data is aggregated at runtime, and a wider range may increase query latency.

\[Omitted image "now-assist-center-auto-eval.png"\] Alt text: AI Admin Center Auto Eval dashboard showing KPI cards and an asset list with evaluation status and benchmark results.

-   **Assets evaluated**

    This area of the dashboard displays the number of assets with at least one evaluation run in the selected date range. The count is shown out of the total assets on the instance.

-   **Risk \(live without evaluation\)**

    This area of the dashboard displays the number of active assets that have not been evaluated. Assets in this state are deployed without quality validation from an evaluation run.

-   **Assist consumption**

    This area of the dashboard displays the total number of assists consumed by evaluation runs in the selected date range.


## All assets

The **All assets** table lists the AI assets on your instance with their evaluation status and benchmark results. Use the search box and **Status** filter to refine the list. Select **Reset** to clear all filters.

-   **Asset name**

    The name of the AI asset. Select the name to open the evaluation detail page for that asset.

-   **Asset type**

    The type of AI asset, such as Agent or Skill.

-   **Status**

    The current evaluation status of the asset.

-   **Eval Runs**

    The total number of evaluation runs completed for the asset.

-   **Benchmarks**

    The benchmarks tested in the most recent evaluation run, such as Time Taken, Offensiveness, and Prompt Injection.

-   **Total Assist consumed**

    The total number of assists consumed across all evaluation runs for the asset.

-   **Last evaluated**

    The date and time of the most recent evaluation run.


## Evaluation detail page

Select an asset name to open the evaluation detail page for that asset.

\[Omitted image "now-assist-center-auto-eval-detail.png"\] Alt text: Evaluation detail page showing asset metadata, benchmark score cards, an evaluations table, and a benchmark trend chart.

-   **Benchmarks**

    This area of the page displays benchmark score cards for each benchmark in the most recent run. Each card shows the score as a percentage and a performance label.

-   **All evaluations**

    This area of the page displays a paginated table of all evaluation runs for the asset. Columns include Run, Data set, Duration, Benchmarks, Date, and Assist consumed.

-   **Benchmark trend**

    This area of the page displays a line chart showing how benchmark scores changed over time across all evaluation runs.


**Parent Topic:**[View AI assets usage and performance in AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-center-view-ai-usage.md)

