---
title: Custom metrics in AI Admin Center \(Lux UI\)
description: Create custom metrics to define the criteria for measuring AI assistant performance, including custom deflection rates based on event-based condition logic.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-admin-center-custom-metric.html
release: australia
topic_type: concept
last_updated: "2026-10-01"
reading_time_minutes: 3
keywords: [AI Admin Center, Now Assist Center, custom metric, deflection, AI analytics, assistants]
breadcrumb: [View AI assets usage and performance \(Lux UI\), Monitor, AI Admin Center, Getting started with AI, Enable AI Experiences]
---

# Custom metrics in AI Admin Center \(Lux UI\)

Create custom metrics to define the criteria for measuring AI assistant performance, including custom deflection rates based on event-based condition logic.

**Important:** Lux is the new user experience for AI Admin Center. For more information on the Lux experience, see [AI Admin Center user experience \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-admin-center-lux-user-experience.md).

The Next Experience AI Admin Center workspace is being prepared for future deprecation and will no longer be supported. For more information on the Next Experience UI, see [AI Admin Center workspace \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-center-workspace.md).

In AI Admin Center version 6.1, the Next Experience and Lux user interfaces are both available.

**Note:** This topic describes the AI Admin Center feature based on the Lux user experience \(UI\). There is no Next Experience UI version of this topic.

## Custom Metrics

The Custom Metrics section in AI Admin Center allows you to define custom metrics for measuring AI assistant performance. A custom deflection metric determines the criteria for counting an AI assistant interaction as deflected. A deflected interaction is one in which the assistant resolved the user's need without escalation to a human agent.

The platform includes a system-provided default metric. You can create custom metrics that reflect your organization's specific deflection criteria. Each AI assistant can be mapped to one active metric at a time.

**Important:**

Set the `sn_nowassist_va.analytics.persistence_strategy` system property to `both` so that granular feedback and event data write to the ServiceNow Otto for Virtual Agent event tables that the condition builder evaluates. This data doesn't include events from other AI surfaces, such as AI Search or in-product skills. Custom metrics built on Feedback or Event type conditions require this data to return results.

## Custom metrics list

The Custom Metrics page lists all metrics available in your organization. System-provided metrics and custom metrics are visually distinguished in the list. Select **New metric** to create a metric; for steps, see [Create a custom metric in AI Admin Center \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-admin-center-create-custom-metric.md). Use the search field above the list to filter metrics by name.

\[Omitted image "ai-admin-center-custom-metric-list.png"\] Alt text: Custom Metric tab showing the Metrics list and Assistants table with metric mappings.

-   **Name**

    This area of the page displays the name of the custom metric.

-   **Metric type**

    This area of the page displays the type of metric as a badge, either **Out of the box** for the system-provided default metric or **Custom** for a metric that you create.

-   **Status**

    This area of the page displays whether the metric is active or inactive.

-   **Assistants**

    This area of the page displays the number of AI assistants currently mapped to this metric.


Hover over the **Metric Type** and **Assistants** column headers for a description of each field.

## Assistant mapping

Each AI assistant can be mapped to one custom metric at a time. When a custom metric is active for a mapped assistant, the deflection card on the assistant's Performance view shows the active metric name. For steps to map an assistant to a metric, see [Edit a custom metric in AI Admin Center \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-admin-center-edit-custom-metric.md).

The Custom Metrics page also lists all AI assistants in an Assistants table below the metrics list. This table shows each assistant's name and the metric it is currently mapped to, in the **Mapped to** column. Use the search field above the table to filter assistants by name.

-   **[Create a custom metric in AI Admin Center \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-admin-center-create-custom-metric.md)**  
Create a custom metric by specifying event-based condition logic and testing it against live data before saving.
-   **[Edit a custom metric in AI Admin Center \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-admin-center-edit-custom-metric.md)**  
Update a custom metric's condition logic, map AI assistants to it, and activate or deactivate it.

**Parent Topic:**[View AI assets usage and performance in AI Admin Center \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-admin-center-lux-view-ai-usage.md)

