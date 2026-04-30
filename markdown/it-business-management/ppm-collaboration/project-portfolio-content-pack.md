---
title: Project Portfolio Management Platform Analytics Solutions
description: Platform Analytics Solutions contain preconfigured dashboards. These dashboards contain actionable data visualizations that help you improve your business processes and practices.
locale: en-US
release: yokohama
product: PPM Collaboration
classification: ppm-collaboration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Project Portfolio Management, Strategic Portfolio Management]
---

# Project Portfolio Management Platform Analytics Solutions

Platform Analytics Solutions contain preconfigured dashboards. These dashboards contain actionable data visualizations that help you improve your business processes and practices.

Platform Analytics data visualizations use Performance Analytics [indicator](https://www.servicenow.com/docs/access?context=now-platform-glossary&version=yokohama&pubname=yokohama-glossary&section=gloss-indicator&ft:locale=en-US) data to show you data over time, helping you analyze your business processes and identify areas of improvement. With Platform Analytics Solutions, you can get value from Performance Analytics for your application with minimal setup. You can always create your own objects as well.

To enable the solution for Project Portfolio Management, log in as an admin and navigate to **Performance Analytics** &gt; **Guided Setup**. Click **Get Started**, then scroll to the section for PPM Standard Dashboards. The guided setup takes you through the entire setup and configuration process.

Alternatively, activate the Performance Analytics – Content Pack – PPM Standard plugin \(com.snc.pa.pmo\_dashboards\).

Activation of com.snc.pa.pmo\_dashboards plugin also activates the following plugins:

-   PPM Standard \(com.snc.financial\_planning\_pmo\)
-   Performance Analytics – Content Pack – Project Portfolio Suite Dashboards \(com.snc.pps\_dashboards\)

Access the PMO dashboard using either of the following navigation links:

-   **Project** &gt; **Portfolios** &gt; **Portfolio Dashboard**.
-   **Project** &gt; **Programs** &gt; **Program Dashboard**.
-   **Self-Service** &gt; **Dashboards**. Search for **PMO Dashboard** using the search field.
-   **Time Sheets** &gt; **Time Sheet Portal** &gt; **Time Sheet Dashboard**.

The dashboard displays the data based on the navigation link used to open it.

## Domain separation and 'Run As' user

In some solutions, System Administrator is the **Run As** user for data collection jobs in the Platform Analytics Solutions. In other solutions, the **Run As** user for data collection jobs is left blank. Verify that the **Run As** user exists on the instance, and that this user has the appropriate level of access. An inappropriate **Run As** user can cause errors or limit the data that is collected. This setting only has an effect if domain separation is enabled.

## Older version of this solution

This solution replaces the Project Portfolio Suite \(com.snc.pa.ppm\) Solution. If you activated an earlier version of the solution and then upgraded your instance, you still have and can still use the earlier solution. You can also activate the newer version without losing data from existing indicators and breakdowns. If you activate the newer version, run a historical data collection job to populate new indicators and breakdowns for the Time Sheet dashboard.

-   **[PMO dashboard](pmo-dashboard.md)**  
The PMO dashboard provides comprehensive reports to the portfolio and program managers. The dashboard uses Platform Analytics to provide a trend of historical data as well as regular reports. It gives an overview of your investments, provides a pipeline view of upcoming intake and a calendar view of upcoming dates.
-   **[Analytics Time sheet](time-sheet-dashboard.md)**  
The Analytics Time sheet provides comprehensive time sheet activities and reports to the time card approvers and time card users. The dashboard uses Performance Analytics to provide a trend of historical data and regular reports. It gives an overview of the time sheet activities of resources, time sheet approval and rejection rate, over-allocated and under-allocated resource counts.

**Parent Topic:**[Project Portfolio Management](../../../product/project-portfolio-suite/concept/c_ProjectPortfolioSuite.md)

**Related topics**  


[Platform Analytics Solutions](https://www.servicenow.com/docs/access?context=content-packs-in-form-analytics&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)

[Activate your Performance Analytics subscription](https://www.servicenow.com/docs/access?context=c_PremiumPerformanceAnalytics&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)

