---
title: Guided Self-Service user experience analytics
description: Visually analyze Guided Self-Service usage, user behavior, and other information from the user experience dashboard.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/employee-service-management/employee-experience-foundation/user-analytics-guided-help-gss.html
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Guided Self-Service in Employee Center, Setup browse experience features, Configure, Employee Center, Employee Service Management]
---

# Guided Self-Service user experience analytics

Visually analyze Guided Self-Service usage, user behavior, and other information from the user experience dashboard.

You can use the dashboard to view the information about the Guided Self-Service usage, engagement, and adoption.

Navigate to **User Experience Analytics** &gt; **Dashboard** &gt; **Guided Self-Service** for a detailed view and analysis. Click the respective widget or chart for more information. You can create a funnel to track session adoption and abandonment.

## Widgets

The dashboard provides the following metrics:

-   **Page Id**: Indicates the occurrences based on the page Id.
-   **Title**: Indicates the occurrences based on the title of the Guided Self-Service.
-   **Source**: Indicates the occurrences based on the source such as Quick link.
-   **User Id**: Indicates the occurrences based on the user.
-   **Events**: Indicates the events based on the user.
-   **Retention**: Indicates the retention info.
-   **Funnel**: Indicates the funnel details based on the user.

\[Omitted image "user-exp-analytics-guided-self-service.png"\] Alt text: Guided Self-Service dashboard for illustration

## User and roles

|Users|Required role|
|-----|-------------|
|Analytics portal admin|portal\_analytics\_admin|
|Analytics viewer|analytics\_viewer, mobile\_analytics\_viewer, web\_analytics\_viewer, portal\_analytics\_viewer|

## User behavior

View and analyze the information available in your dashboard. You can track user behavior and app usage on the app launcher.

-   View the Guided Self-Service that employees launch frequently.
-   Track monthly and daily user activity.
-   View number of user clicks by Guided Self-Service from home page, topic page, and quick links.
-   Analyze the trend of user activity periodically.
-   Assess the user behavior and insights and drive business decisions.

## Events

Events list can help you understand usage patterns, features popularity, and identify areas for improvement.

-   Click Declarative Action: A declarative action that the user clicked such as restart, start over, continue, complete, edit responses.
-   Page Navigate: A user navigates to Guided Self Service page.
-   Guided Self-service Catalog item shown: The self-service catalog item that the user interacted with.
-   Guided Self-service Knowledge article shown: the self-service knowledge base articles that the user interacted with.
-   PLAYBOOK\_COMPLETED: A guided process \(playbook\) that the user completed.
-   Guided Self-service Action clicked: The action button that the user clicked.

For more information, see [Events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/now-intelligence/usage-insights/view-events.md).

## Funnel analysis

A funnel analysis shows the percentage of users who completed a desired Guided Self-Service action along a critical path. Funnel reports show conversion rates and trends in aggregate user behavior to uncover the reasons behind success or failure of a specific Guided Self-Service flow.

For more information, see [Funnel reports in User Experience Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/now-intelligence/usage-insights/funnel-reports-uxa.md).

## Retention

View data such as how many new users you have and how many returned. User retention data also shows you the frequency of user sessions and the average time in between sessions given a certain time period.

For more information, see [User retention](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/now-intelligence/usage-insights/view-retention-analytics.md).

