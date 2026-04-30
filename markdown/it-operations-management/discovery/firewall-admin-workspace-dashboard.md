---
title: Firewall Admin Workspace dashboard
description: The unified dashboard enables security and risk teams to oversee tasks, change requests, and the entire firewall inventory life cycle, with daily or manual updates for accurate and current information.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Firewall Audits and Reporting reference, Firewall Audits and Reporting, Discovery, ITOM Visibility, IT Operations Management]
---

# Firewall Admin Workspace dashboard

The unified dashboard enables security and risk teams to oversee tasks, change requests, and the entire firewall inventory life cycle, with daily or manual updates for accurate and current information.

## Firewall Insights tab

The **Insights** tab offers a snapshot of firewall policies and associated devices, showcasing trends in policies without owners over time. Track new and unaudited policies, and view the distribution of device manufacturers and models within the network.

![The Firewall Insights tab visualizes the data of the firewall records tables.](../image/firewall-insights-tab.png)

## Requests and Audits tab

Within the **Tasks** tab, explore the **Requests** and **Audits** sub-tabs. The **Requests** tab provides breakdowns of request tasks by state and ownership, along with fulfillment trends over time. Similarly, the **Audits** tab displays outstanding audits by state and ownership, along with response trends over time.

![Select the requests sub-tab near the top of the page.](../image/firewall-requests-tab.png)![Select the audits sub-tab near the top of the page.](../image/firewall-audits-tab.png)

## Firewall Records tab

The **Firewall Records** tab offers consolidated access to Records, Rules Requests, and Audits tables. Users can filter, edit, and export individual or groups of records. The **Devices** and **Security Policy** sub-tabs feature a dependency viewer for selected records.

![The Firewall Records tab displays categories on the sidebar, and records in the tables.](../image/firewall-records-tab.png)

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|Risk teams|firewall\_admin or firewall\_user|
|Security|firewall\_admin or firewall\_user|

## Use case

To update the dashboard manually, navigate to **Performance Analytics** &gt; **Data Collector** &gt; **Jobs** and select **Firewall Scheduled Job**. Open the record and select **Execute Now** to update the dashboard elements with the latest information.

**Parent Topic:**[Firewall Audits and Reporting reference](../reference/firewall-audit-report-reference.md)

