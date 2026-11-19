---
title: Rationalization of business applications
description: As an Enterprise Architect, you can use application rationalization to evaluate your business applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-portfolio-management/eaw-rationalize-business-applications.html
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Rationalization of business applications

As an Enterprise Architect, you can use application rationalization to evaluate your business applications.

## Application rationalization overview

Rationalize all business applications in a category and decide whether to invest, sustain, migrate, or retire an application.

Select the application rationalization icon \(\[Omitted image "icon-app-rationalization.png"\] Alt text: Application rationalization icon.\) to navigate to the Application Rationalization page.

You can perform the following using application rationalization:

-   Analyze business applications based on multiple scores.
-   Create a demand for a business application.
-   Set the planned disposition of a business application.
-   Add life-cycle details to an existing business application.

You can view all the business applications in a bubble chart view or in a list view. However, business applications marked as **Retired** or in **End of Life** lifecycle stage aren’t displayed on the Application Rationalization bubble chart or list view pages. However, you can view those business applications by updating the **sn\_apm\_ws.business\_application\_default\_filter** system property. Contact your ServiceNow® account service manager to update the system property.

You can also generate insights into business applications using Now Assist. For information, see [Generate insights into business applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/generate-insights-into-ba.md).

\[Omitted image "bubble-chart-view.png"\] Alt text: Bubble chart view in the Application Rationalization page.

\[Omitted image "eaw-list-view.png"\] Alt text: List view in the Application Rationalization page.

## Application rationalization insights on the Enterprise Architecture Workspace home page

The application rationalization feature of Application Portfolio Management also provides insights for your business applications. To see the insight cards, navigate to **Workspaces** &gt; **Enterprise Architecture Workspace** and select the Insights section. The insights cards display information based on scores derived from application rationalization. The following insight cards are available:

-   **Candidate business applications for retirement**-business applications that might fit for retirement based on their indicator scores.
-   **Candidate business applications for migration**-business applications that might fit for migration based on their indicator scores.
-   **Candidate business applications for investment**-business applications that might fit for investment based on their indicator scores.
-   **Candidate business applications with mismatch planned disposition**-business application with mismatch between their planned disposition and their indicator scores.

\[Omitted image "app-rat-card-homepage.png"\] Alt text: Application rationalization cards highlighted on the Home page of EA Workspace.

On selecting a particular card, the Application Rationalization page appears to display the relevant business application data, based on your selection.

**Note:** To return to the main Application Rationalization page, select **Go to Application Rationalization**.

\[Omitted image "app-rat-back-button.png"\] Alt text: Go to Application Rationalization button highlighted on the application rationalization list view page.

## Indicator scores based on fiscal period

All the indicator scores are displayed according to the latest fiscal period, by default. You can also select a different fiscal period from the Scores for fiscal period list. Your fiscal period preferences are saved and applied the next time you visit the page.

\[Omitted image "fiscal-period-dropdown.png"\] Alt text: Scores for fiscal period list highlighted on the Application rationalization list view page.

The latest fiscal period is derived from the apm\_app\_indicator\_score list. The fiscal period type \(month, quarter, or year\) is derived from the system property **com.glide.fiscal\_calendar.fiscal\_unit**.

**Note:** You can zoom on this page to 200% or 400% through your browser settings without the loss of content or functionality. Page layouts are transformed into a vertical, stacked view automatically.

-   **[Bubble chart view of application rationalization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/eaw-bubble-chart-view.md)**  
Bubble charts are interactive graphs that position applications in different quadrants, based on their indicator scores. Based on the position of the business application in the quadrants, enterprise architects can take decisions to invest in, sustain, migrate, or retire the business applications.
-   **[List view of application rationalization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/eaw-list-view.md)**  
As an Enterprise Architect, you can view the list of all business applications. The List view enables you to see high-level information on all your business applications and all the indicator scores that are attached to them.
-   **[Apply filters on the Application Rationalization page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/eaw-apply-filters-app-rat.md)**  
You can apply filters on the Application Rationalization page in the Enterprise Architecture Workspace. Based on the applied filters, the bubble chart and list view are updated so that you can view data for a specific business application. Your filter preferences are saved and applied the next time you visit the page.

**Parent Topic:**[Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/ea-workspace.md)

**Related topics**  


[Generate insights into business applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/generate-insights-into-ba.md)

