---
title: Working with the Health and Safety dashboard
description: With the Health and Safety dashboard, you can actively monitor and manage workplace safety performance across different locations in your organization and identify areas needing attention.
locale: en-US
release: xanadu
product: Health and Safety Core
classification: health-and-safety-core
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Health and Safety Core, Health and Safety, Employee Service Management]
---

# Working with the Health and Safety dashboard

With the Health and Safety dashboard, you can actively monitor and manage workplace safety performance across different locations in your organization and identify areas needing attention.

![Health and Safety dashboard showing safety incidents metrics in the Highlights, Incident Management, and Risk Management tabs.](../image/hs-health-safety-dashboard.gif)

## Key features of the dashboard

-   The dashboard provides a centralized view of key safety indicators such as incident counts, recordable injuries, and safety action status. You can monitor the status, see trends, and drill down into the details from a single view.
-   The available filters help you to refine the view by date range, region, site, campus, building, and floor.
-   Depending on your role, the dedicated tabs for **Incident Management** and **Risk Management** help you to easily track incidents and assess risks.

## Dashboard tabs

The dashboard features several tabs to enable you to navigate between different areas of workplace safety. The tabs and their widgets are available based on the installed Health and Safety applications in your ServiceNow instance.

-   **Highlights**

    This tab features a selection of key cards from the Incident Management and Risk Management tabs, to provide a high-level summary of key safety metrics such as the total incidents, recordable injuries, and open risk assessments.

-   **Incident Management**

    This tab focuses on tracking and managing safety incidents, injuries, and observations. For detailed information on incident management metrics, see [Monitoring and analyzing safety incident metrics](../../ohs-incident-management/concept/hs-monitoring-analyzing-safety-incident-metrics.md).

-   **Establishment Metrics**

    This tab shows key cards from the Incident Management tab, presented with a breakdown by establishment for more localized insights.

-   **Risk Management**

    This tab shows metrics identifying, assessing, and mitigating risks. For detailed information on safety risk management metrics, see [Monitoring and analyzing safety risk metrics](../../hs-risk-management/concept/hs-monitoring-analyzing-safety-risk-metrics.md).


## Customizing widgets

You can customize the widgets in the dashboard to display relevant metrics by using the UI Builder. For more information, see [UI Builder tutorial](https://www.servicenow.com/docs/access?context=uib-tutorial&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

## Required roles

-   sn\_ohs\_im.manager, sn\_ohs\_im.agent, or sn\_ohs\_im.compliance\_manager, needed to see dashboard home page. The metrics on each tab are dependent on the user's access to that table.
-   sn\_ohs\_im.admin and the following roles, to edit the dashboard:
    -   pa\_admin, to edit the Performance Analytics \(PA\) components used in the dashboard.
    -   ui\_builder\_admin, to edit the dashboard visualizations that are built using the UI Builder.

## Access the Health and Safety dashboard

To open the Health and Safety dashboard, navigate to **Workspaces** &gt; **Health and Safety Workspace**.

**Related topics**  


[Monitoring and analyzing safety incident metrics](../../ohs-incident-management/concept/hs-monitoring-analyzing-safety-incident-metrics.md)

[Monitoring and analyzing safety risk metrics](../../hs-risk-management/concept/hs-monitoring-analyzing-safety-risk-metrics.md)

