---
title: Application Fingerprints dashboard
description: ITOM Visibility uses Predictive Intelligence to perform initial analysis of discovered processes and suggest applications that you might want to discover. When using this method, ITOM Visibility automatically creates a Configuration Management Database \(CMDB\) configuration item \(CI\) class, a classifier, or a pattern for the new application CI class. Use the Application Fingerprints dashboard to review suggested applications.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Discover applications based on fingerprints, Running discoveries in your network, Discovery, ITOM Visibility, IT Operations Management]
---

# Application Fingerprints dashboard

ITOM Visibility uses Predictive Intelligence to perform initial analysis of discovered processes and suggest applications that you might want to discover. When using this method, ITOM Visibility automatically creates a Configuration Management Database \(CMDB\) configuration item \(CI\) class, a classifier, or a pattern for the new application CI class. Use the Application Fingerprints dashboard to review suggested applications.

![Application Fingerprints dashboards](../image/discovery-app-fingerprints-dashboard.png)

## Required ServiceNow AI Platform roles

The discovery\_admin, who runs horizontal discovery using Discovery.

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

|User|Dashboard use|
|----|-------------|
|Administrator performing horizontal discovery of the organization IT network.|Review application suggestions and decide which applications to discover based on fingerprints. Performing this action enhances the results of the basic horizontal discovery.|

## Indicators

-   **Suggested application servers**

    The filtered list of suggestions for application servers.

-   **Suggested applications**

    The complete list of suggestions for applications.

-   **Created applications**

    The list of applications that the system discovered based on fingerprints.


## Data visualizations

<table id="table_xvt_hl4_2fb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Top Suggestions

</td><td>

Pie Chart![Pie Chart icon](../../../reuse/reporting/image/pie-sm.svg)

</td><td>

Application Suggestion \[cmdb\_process\_groups\]

</td><td>

A pie chart report that shows the top suggestions arranged by the number of processes making up these suggestions. The process count is reflected by the size of the chart segment. Click the segment to see its corresponding suggestions in a filtered list. To remove a suggestion from the chart, click the suggestion name in the chart legend.

</td></tr></tbody>
</table>