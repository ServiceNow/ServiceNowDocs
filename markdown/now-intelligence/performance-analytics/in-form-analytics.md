---
title: In-form analytics
description: In-form analytics integrate performance insights into forms so that users can access important metrics in context and make better decisions.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# In-form analytics

In-form analytics integrate performance insights into forms so that users can access important metrics in context and make better decisions.

In-form analytics involve a UI action on a form that opens a view of a dashboard based on a breakdown. This breakdown dashboard provides valuable performance insights to the user who is completing the form. For example, you want support engineers, while creating an incident, to be able to see the expected time to close the incident based on the incident category. To enable the engineers to view this information, you create an in-form analytics UI action for incident forms. This UI action opens an Incident. Category breakdown dashboard with a widget that shows the expected time to close an incident.

**Important:** In-form analytics do not support Platform Analytics artifacts. They open only Core UI responsive dashboards. After full migration to Platform Analytics, in-form analytics are no longer available.

![The breakdown dashboard for an incident form being displayed in a pop-up window when the UI action icon is clicked.](../image/in-form-analytics-category.png "Incident: Category in-form analytics")

The UI action for in-form analytics is activated through an icon next to the field on the form that represents the breakdown. If that field is not visible in the form view, neither is the icon. When you set up in-form analytics, you have the option of also including a Related Action link on the form. This link is always available.

-   **[Add in-form analytics to a form](../task/t_CreateInFormAnalyticsAction.md)**  
Create a UI action that enables users to view relevant analytics while completing a form. The UI action associates the table that uses the form, a breakdown used with that table, and a breakdown dashboard.
-   **[Preconfigured in-form analytics](../../dashboards/reference/available-in-form-analytics.md)**  
Preconfigured in-form analytics are available as plugins for several applications and their associated tables and forms.

**Parent Topic:**[Configure Performance Analytics fundamentals](c_PAWidgetsAndDashboards.md)

**Related topics**  


[Using breakdowns on dashboards](c_SpecialDashboards.md)

[bundle-platadm.c_UIActions]

