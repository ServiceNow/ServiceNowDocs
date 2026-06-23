---
title: Reporting incidents
description: Service desk and other IT managers can use dashboards and reports to monitor and track incident status and service levels.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-service-management/incident-management/incident-monitor-track.html
release: yokohama
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Incident Management, IT Service Management]
---

# Reporting incidents

Service desk and other IT managers can use dashboards and reports to monitor and track incident status and service levels.

## Incident Overview

The **Incident** &gt; **Overview** dashboard provides a quick glance at the current state of open incidents. At the top, single score widgets enumerate the open incident statuses, such as critical incidents, unassigned incidents, and overdue incidents. Charts in the dashboard group incidents by factors such as priority and state. The incident overview is fully interactive and configurable.

## Incident reports

Various incident reports are available in the base system, and you can modify the existing reports or create new ones. Navigate to **Reports** &gt; **View / Run** and enter `incident` in the search box to view all incident reports. Base system reports include the following:

-   Basic bar or pie chart reports, such as incidents by assignment group, location, priority, or state. These reports help you analyze a specific data point, for example, whether enough staff is allocated to an assignment group.
-   Time series reports, such as **Incident Trend by Configuration Item**. This report lets you analyze closed incidents by configuration item \(CI\) to identify potential problems.
-   Multidimensional reports, such as **Incidents by Priority and State older than 30 Days**. This report can help you identify gaps in service levels. For example, if a high number of low-priority incidents are still in **New** state after being open more than 30 days.

## Incident metric definition

A metric measures and evaluates the effectiveness of IT service management processes. The service desk can improve the incident management process using information gathered within the platform. You can activate the Metric Definition plugin \(com.glide.metrics\) and define the metrics to monitor within the system. With these metrics, and the information within the database, it is possible to [generate reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/reporting/t_CreateYourOwnReport.md) that can be [added to dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/reporting/add-report-to-dashboard.md) or [automatically generated and distributed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/time-configuration/t_CreateAScheduledJob.md).

Using this information, it is possible to refine automatic rules such as the assignment rules, service level agreements, or inactivity monitors to better suit the unique environment of the service desk. Unnecessary incidents can be avoided by encouraging users to consult the knowledge base before creating an incident. The related search results function in the Incident form assists with this strategy.

## Complimentary Performance Analytics for Incident Management

Complimentary Performance Analytics for Incident Management and aggregates data over time, and is enabled by default for Incident Management. Complimentary Performance Analytics for Incident Management provides an Incident Management dashboard with 15 indicators to help you assess organizational performance. For more information, see [Performance Analytics for Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/performance-analytics/r_StUpPAInctMgmt.md).

If you subscribe to Performance Analytics, additional [Platform Analytics Solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/platform-analytics/content-packs-in-form-analytics.md) are available for Incident Management. The Platform Analytics Solution for Incident Management contains preconfigured dashboards.

A subscription to Performance Analytics also gives you access to In-form analytics. In-form analytics integrate performance insights into Incident records so that users can access important metrics in context and make better decisions. For more information, see [Text-To-Display](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/performance-analytics/in-form-analytics.md).

-   **[Legacy: Incident Management Platform Analytics Solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-service-management/incident-management/incident-content-pack.md)**  
Platform Analytics Solutions and in-form analytics contain preconfigured dashboards. These dashboards contain actionable data visualizations that help you improve your business processes and practices.
-   **[Legacy: Incident SLA Management Platform Analytics Solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-service-management/incident-management/incident-sla-content-pack.md)**  
Platform Analytics Solutions contain preconfigured dashboards. These dashboards contain actionable data visualizations that help you improve your business processes and practices.

**Parent Topic:**[Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-service-management/incident-management/c_IncidentManagement.md)

**Related topics**  


[Creating reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/reporting/report-types-creation-details-rd.md)

