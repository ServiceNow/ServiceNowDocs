---
title: Insights and Opportunities for Incident dashboard reference
description: Reference information for the widgets on the Insights and Opportunities for Incident dashboard, including descriptions of each indicator and the data it presents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/now-assist-for-it-service-management-itsm/insights-opportunities-incident-dashboard-reference.html
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: reference
last_updated: "2026-06-04"
reading_time_minutes: 4
keywords: [Insights and Opportunities, incident, dashboard, ITSM, Service Operations Workspace, insights and opportunities, widgets, SLA, sentiment, incident trends, channel distribution, reassignment]
audience: user
breadcrumb: [Insights and Opportunities for Incident dashboard, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Insights and Opportunities for Incident dashboard reference

Reference information for the widgets on the Insights and Opportunities for Incident dashboard, including descriptions of each indicator and the data it presents.

## KPI widgets

|Widget|Description|
|------|-----------|
|Incident volume|The total number of incidents created within the selected date range. Displays the count alongside a comparison to the previous period and a trend line showing volume over time. Use this widget to understand overall support demand and identify significant changes in incident intake.|
|SLA status|A bar chart showing the number of incidents that are on track vs. breached against their SLA targets. Use this widget to quickly assess service delivery compliance and identify whether SLA breach rates require attention.|
|Incident sentiment trend|A line chart showing the AI-inferred sentiment score of incident interactions over time. Scores range from negative to positive, reflecting the overall tone and quality of incident interactions. Use this widget to track whether sentiment is improving or declining across the selected period.|

## Incident trends

|Widget|Description|
|------|-----------|
|Incident trends|A sortable table listing incident trend categories, clustered by recurring themes, and ranked by total incident count. Use this table to identify recurring issues that may benefit from problem management, knowledge articles, or automation. Select a row in the table to open the trend category view.|

## Distribution widgets

|Widget|Description|
|------|-----------|
|Top departments|A horizontal bar chart showing the departments with the highest incident volume. Use this widget to understand which parts of the organization are generating the most support demand and to align staffing or self-service capabilities accordingly.|
|Geographic distribution of incidents|A world map visualization showing the geographic distribution of incidents by location. Use this widget to identify regional support patterns, plan coverage, and verify resources are aligned with demand across locations.|
|Channel distribution|A donut chart showing the proportion of incidents submitted through each channel, such as phone, self-service, email, chat, portal, and walk-in. Use this widget to understand how users are reaching support and to evaluate channel adoption and effectiveness.|
|Services by business criticality|A bar chart showing incident volume grouped by the business criticality of the affected service. Use this widget to prioritize response efforts and assess exposure across services of varying criticality levels.|

## Table widgets

|Widget|Description|
|------|-----------|
|Top configuration item classes|A table listing configuration item \(CI\) classes alongside the number of configuration items and total incidents associated with each class. Use this table to identify which CI types are most frequently involved in incidents and to focus asset management or change efforts accordingly.|
|Top assignment groups with high reassignment count|A table listing assignment groups ranked by total reassignments, alongside the total incident count for each group. Use this table to identify routing inefficiencies, skill gaps, or capacity issues that are causing incidents to be reassigned multiple times before resolution.|

## Trend category view widgets

The trend category view includes all Dashboard view widgets scoped to the selected trend category. The following widgets are unique to the trend category view.

|Widget|Description|
|------|-----------|
|Summary|An AI-generated natural language summary of the selected trend category, including identified issues and probable causes derived from the associated incident records. Select **Show more** to expand the full summary. The summary may not reflect all details of the trend category. Review the associated incident records to verify accuracy before taking action.|
|Total incidents|The total number of incidents in the selected trend category within the selected date range.|
|Average MTTR|The average mean time to resolve \(MTTR\) for incidents in the selected trend category. Displays a note when insufficient data is available to calculate the value.|
|SLA breached incidents|The number of incidents in the selected trend category that have breached their SLA targets.|
|Total reassignments|The total number of reassignments across all incidents in the selected trend category.|
|Incident priority breakdown|A bar chart showing the distribution of incidents in the selected trend category by priority level. Use this widget to assess the severity profile of the trend category.|
|Top categories|A donut chart showing the distribution of incidents in the selected trend category by category. Use this widget to identify the most common incident categories within the trend category.|
|Top 10 departments by volume|A grouped bar chart showing incident volume by department, broken down by incident state. Use this widget to identify which departments are most affected and how incidents are progressing.|
|Top assignment group by MTTR|A line chart showing MTTR trends over time for each assignment group associated with the selected trend category. Use this widget to compare resolution efficiency across groups.|
|SLA-breached open incidents|A table listing open incidents that have breached their SLA, including the overdue duration, assignment group, and assignee. Use this table to identify and act on the most time-sensitive open incidents.|
|Associated incidents|A full list of incidents in the selected trend category. Columns include incident number, opened date, short description, caller, sentiment, sentiment trend, priority, state, category, assignment group, and assignee. Select an incident number to open the incident record.|

