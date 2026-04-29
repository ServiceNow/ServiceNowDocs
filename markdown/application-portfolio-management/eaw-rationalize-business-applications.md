---
title: Rationalization of business applications
description: As an Enterprise Architect, you can use application rationalization to evaluate your business applications.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
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

You can view all the business applications in a bubble chart view or in a list view. However, business applications marked as **Retired** or in **End of Life** lifecycle stage aren’t displayed on the Application Rationalization bubble chart or list view pages. However, you can view those business applications by updating the **sn\_apm\_ws.business\_application\_default\_filter** system property. Contact your ServiceNow® account service manager to update the system property.

You can also generate insights into business applications using Now Assist. For information, see [Generate insights into business applications](../../../now-assist-ea/task/generate-insights-into-ba.md).

![Bubble chart view in the Application Rationalization page.](../../image/eaw-image/bubble-chart-view.png "Bubble chart view")

![List view in the Application Rationalization page.](../../image/eaw-image/eaw-list-view.png "List view")

## Application rationalization insights on the Enterprise Architecture Workspace home page

The application rationalization feature of Application Portfolio Management also provides insights for your business applications. To see the insight cards, navigate to **Workspaces** &gt; **Enterprise Architecture Workspace** and select the Insights section. The insights cards display information based on scores derived from application rationalization. The following insight cards are available:

-   **Candidate business applications for retirement**-business applications that might fit for retirement based on their indicator scores.
-   **Candidate business applications for migration**-business applications that might fit for migration based on their indicator scores.
-   **Candidate business applications for investment**-business applications that might fit for investment based on their indicator scores.
-   **Candidate business applications with mismatch planned disposition**-business application with mismatch between their planned disposition and their indicator scores.

![Application rationalization cards highlighted on the Home page of EA Workspace.](../../image/eaw-image/app-rat-card-homepage.png)

On selecting a particular card, the Application Rationalization page appears to display the relevant business application data, based on your selection.

**Note:** To return to the main Application Rationalization page, select **Go to Application Rationalization**.

![Go to Application Rationalization button highlighted on the application rationalization list view page.](../../image/eaw-image/app-rat-back-button.png)

## Indicator scores based on fiscal period

All the indicator scores are displayed according to the latest fiscal period, by default. You can also select a different fiscal period from the Scores for fiscal period list. Your fiscal period preferences are saved and applied the next time you visit the page.

![Scores for fiscal period list highlighted on the Application rationalization list view page.](../../image/eaw-image/fiscal-period-dropdown.png)

The latest fiscal period is derived from the apm\_app\_indicator\_score list. The fiscal period type \(month, quarter, or year\) is derived from the system property **com.glide.fiscal\_calendar.fiscal\_unit**.

**Note:** You can zoom on this page to 200% or 400% through your browser settings without the loss of content or functionality. Page layouts are transformed into a vertical, stacked view automatically.

-   **[Bubble chart view of application rationalization](eaw-bubble-chart-view.md)**  
Bubble charts are interactive graphs that position applications in different quadrants, based on their indicator scores. Based on the position of the business application in the quadrants, enterprise architects can take decisions to invest in, sustain, migrate, or retire the business applications.
-   **[List view of application rationalization](eaw-list-view.md)**  
As an Enterprise Architect, you can view the list of all business applications. The List view enables you to see high-level information on all your business applications and all the indicator scores that are attached to them.
-   **[Tech debt indicator score for application rationalization](../../reference/eaw-reference/trm-tech-debt-indicator-for-app-rat.md)**  
The Technology Reference Model \(TRM\) Technical Debt indicator is a customizable application metric that evaluates the technical debt score for each Business Application. This score reflects the number of associated technologies that don’t comply with established TRM standards. It offers a clear and measurable value that can be leveraged across the Enterprise Architecture workspace for scoring, analysis, and visualization.

**Parent Topic:**[Exploring Enterprise Architecture Workspace](../explore-eaw.md)

**Related topics**  


[Working with application rationalization](eaw-work-with-app-rat.md)

[Generate insights into business applications](../../../now-assist-ea/task/generate-insights-into-ba.md)

