---
title: Insights into failed scenarios
description: Analyze failed scenarios in an automated evaluation and see the recurring failure patterns behind them, to prioritize what to fix without reviewing every failed scenario one by one.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/conversational-interfaces/now-assist-in-virtual-agent/severity-insights.html
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2026-10-05"
reading_time_minutes: 2
breadcrumb: [Testing assistant conversations, ServiceNow Otto for Virtual Agent, Conversational Interfaces]
---

# Insights into failed scenarios

Analyze failed scenarios in an automated evaluation and see the recurring failure patterns behind them, to prioritize what to fix without reviewing every failed scenario one by one.

## View top failure patterns

After an automated evaluation with failed scenarios finishes running, Assistant Designer analyzes the failed scenarios and clusters them into failure patterns. The **Top issues detected** section on the evaluation results page lists these patterns so you can see where your assistant is breaking down across the whole data set.

\[Omitted image "severity-insights-01.png"\] Alt text: Evaluation results page showing the metric scores and the Top issues detected section.

By default, up to four failure patterns are shown, ranked by severity and then by frequency, from highest to lowest. You can:

-   Sort the list by **Severity** or **Frequency**.
-   Select **Show issues** to expand the list and view every failure pattern that was detected.
-   Select **View scenarios** next to a failure pattern to see the specific scenarios where it occurred.

## View scenarios for a failure pattern

Select **View scenarios** from either the **Top issues detected** list or a metric's issue chart to open the **Scenarios** list, filtered to the scenarios where that failure pattern occurred. If you select more than one failure pattern, the list shows the scenarios where any of the selected patterns occurred.

\[Omitted image "severity-insights-03.png"\] Alt text: Scenario list filtered by issue types detected.

The list includes:

-   **Scenario**: The scenario name, which links to the scenario's transcript.
-   **Issues detected**: The failure patterns found in that scenario, grouped by metric category.

By default, scenarios are sorted by severity and then alphabetically. Select a column header to sort by **Scenario** or **Issues detected** instead.

## View a scenario transcript

Select a scenario name from the **Scenario** list to open its transcript.

\[Omitted image "severity-insights-04.png"\] Alt text: Scenario transcript with the Why was this flagged panel.

The transcript page shows:

-   The full conversation transcript. Select **Download** to save the transcript as a CSV file.
-   **Why was this flagged?**: Every issue detected in the scenario, along with an explanation, sorted by severity from highest to lowest.

**Note:** An issue tied to a per-conversation metric isn't associated with a specific turn in the transcript. An issue tied to a per-turn metric is labeled at the turn where it occurred, when possible.

Select **Back to list of scenarios** to return to the filtered scenario list.

**Related topics**  


[Testing assistant conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/now-assist-in-virtual-agent/evaluations-ad.md)

[Customizing severity levels](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/now-assist-in-virtual-agent/customize-severity-levels.md)

[Evaluation metrics for automated evaluation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/now-assist-in-virtual-agent/evaluation-metrics-auto-eval-ad.md)

