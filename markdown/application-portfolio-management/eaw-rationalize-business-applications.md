---
title: Rationalization of business applications
description: As an Enterprise Architect, you can use application rationalization to evaluate your business applications.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Rationalization of business applications

As an Enterprise Architect, you can use application rationalization to evaluate your business applications.

## Application rationalization overview

Rationalize all business applications in a category and decide whether to invest, sustain, migrate, or retire an application.

Select the application rationalization icon \(![Application rationalization icon.](../../image/eaw-image/icon-app-rationalization.png)\) to navigate to the Application Rationalization page.

You can perform the following using application rationalization:

-   Analyze business applications based on multiple scores.
-   Create a demand for a business application.
-   Set the planned disposition of a business application.
-   Add life-cycle details to an existing business application.

Use the following filters to narrow down the list of business applications:

-   Fiscal Period
-   Application Category
-   Application Family
-   Business Capability

    **Note:** On applying this filter, all business applications including the ones associated with the child capabilities of the parent capability are displayed.

-   Planned Disposition

You can view all the business applications in a bubble chart view or in a list view.

**Note:**

You need Enterprise Architecture Workspace version 2.2.0 to view the Application Rationalization page.

![Bubble chart view in the Application Rationalization page.](../../image/eaw-image/bubble-chart-view.png "Bubble chart view")

![List view in the Application Rationalization page.](../../image/eaw-image/eaw-list-view.png "List view")

## Application rationalization insights on the Enterprise Architecture Workspace home page

The application rationalization feature of Application Portfolio Management also provides insights for your business applications. To see the insight cards, navigate to **Workspaces** &gt; **Enterprise Architecture Workspace** and select the Insights section. The insights cards display information based on scores derived from application rationalization. The following insight cards are available:

-   **Candidate business applications for retirement**-business applications that might fit for retirement based on their indicator scores.
-   **Candidate business applications for migration**-business applications that might fit for migration based on their indicator scores.
-   **Candidate business applications for investment**-business applications that might fit for investment based on their indicator scores.
-   **Candidate business applications with mismatch planned disposition**-business application with mismatch between their planned disposition and their indicator scores.

On selecting a particular card, the Application Rationalization page appears to display the relevant business application data, based on your selection.

All the indicator scores are displayed according to the latest fiscal period, by default. The latest fiscal period is derived from the apm\_app\_indicator\_score list. The duration of a fiscal period is derived from the system property **com.glide.fiscal\_calendar.fiscal\_unit**.

**Note:** To return to the main Application Rationalization page, select **Go to Application Rationalization**.

-   **[Bubble chart view of application rationalization](eaw-bubble-chart-view.md)**  
Bubble charts are interactive graphs that position applications in different quadrants, based on their indicator scores. Based on the position of the business application in the quadrants, enterprise architects can take decisions to invest in, sustain, migrate, or retire the business applications.
-   **[List view of application rationalization](eaw-list-view.md)**  
As an Enterprise Architect, you can view the list of all business applications. The List view enables you to see high-level information on all your business applications and all the indicator scores that are attached to them.

**Parent Topic:**[Enterprise Architecture Workspace](../ea-workspace.md)

