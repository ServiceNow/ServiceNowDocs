---
title: Exploring the AI Portfolio tab on the Enterprise Architecture Workspace dashboard
description: The AI Portfolio tab on the Enterprise Architecture Workspace dashboard provides visualization widgets that show how business applications and AI systems in your organization are associated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-dashboard-exploring-ai-portfolio-tab.html
release: australia
topic_type: concept
last_updated: "2026-06-04"
reading_time_minutes: 2
breadcrumb: [Exploring Portfolio list view, Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Exploring the AI Portfolio tab on the Enterprise Architecture Workspace dashboard

The **AI Portfolio** tab on the Enterprise Architecture Workspace dashboard provides visualization widgets that show how business applications and AI systems in your organization are associated.

When the AI Control Tower \(AICT\) workspace is installed, the **AI Portfolio** tab appears on the Enterprise Architecture Workspace dashboard alongside the existing portfolio tabs. Use this tab to monitor AI adoption and understand how business applications and AI systems are connected across your enterprise.

**Note:** The **AI Portfolio** tab is visible only when the AI Control Tower workspace is installed on your instance.

## AI Portfolio widgets

The **AI Portfolio** tab contains two widgets. Both widgets source their data from approved linkage records in the AI System–Business Application relationship table.

\[Omitted image "dashboard-ai-portfolio-tab.png"\] Alt text: AI Portfolio tab in the EA Dashboard page

-   **Business Applications by AI System Association**

    Displays the total count of active business applications in the center of the chart. The chart is segmented into two groups:

    -   **Associated: Linked to AI systems** — Business applications that have at least one approved linkage with an AI system.
    -   **Not associated: Not linked to AI systems** — Business applications with no approved AI system association.
-   **AI Systems by Business Application Association**

    Displays the total count of AI systems in the center of the chart. The chart is segmented into two groups:

    -   **Associated: Linked to business applications** — AI systems that have at least one approved linkage with a business application.
    -   **Not associated: Not linked to business applications** — AI systems with no approved business application association.

If no AI systems are associated with any business applications, the widgets display the default empty state.

**Parent Topic:**[Exploring Portfolio list view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/portfolio-list-view.md)

**Related topics**  


[AI Control Tower integration with Enterprise Architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-aict.md)

[Explore the Enterprise Architecture Workspace dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-workspace-dashboard.md)

[Add an existing AI system to a business application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-add-ai-system-to-ba.md)

[AI Control Tower Home](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower-home-page.md)

