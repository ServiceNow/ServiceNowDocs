---
title: Edit a custom metric in AI Admin Center \(Lux UI\)
description: Update a custom metric's condition logic, map AI assistants to it, and activate or deactivate it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-admin-center-edit-custom-metric.html
release: australia
topic_type: task
last_updated: "2026-10-01"
reading_time_minutes: 3
keywords: [AI Admin Center, Now Assist Center, custom metric, deflection, AI analytics, assistants]
breadcrumb: [Custom metrics \(Lux UI\), View AI assets usage and performance \(Lux UI\), Monitor, AI Admin Center, Getting started with AI, Enable AI Experiences]
---

# Edit a custom metric in AI Admin Center \(Lux UI\)

Update a custom metric's condition logic, map AI assistants to it, and activate or deactivate it.

**Important:** Lux is the new user experience for AI Admin Center. For more information on the Lux experience, see [AI Admin Center user experience \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-admin-center-lux-user-experience.md).

The Next Experience AI Admin Center workspace is being prepared for future deprecation and will no longer be supported. For more information on the Next Experience UI, see [AI Admin Center workspace \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-center-workspace.md).

In AI Admin Center version 6.1, the Next Experience and Lux user interfaces are both available.

## Before you begin

Role required: `ai_engmt_admin`

## About this task

Edit a custom metric to change its condition logic, update which AI assistants are mapped to it, or activate or deactivate it.

**Note:** This topic describes the AI Admin Center feature based on the Lux user experience \(UI\). There is no Next Experience UI version of this topic.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Center** &gt; **Home** or **Admin** &gt; **AI Admin Center**.

2.  Select **Analytics** \(\[Omitted image "icon-aiac-lux-nav-monitor.png"\] Alt text: Analytics icon.\) in the side navigation panel.

3.  Select the **Custom Metric** tab.

4.  Select the name of the metric that you want to edit.

    The Edit metric page opens.

    \[Omitted image "ai-admin-center-custom-metric-edit-screen.png"\] Alt text: Edit metric page showing the Metric Details, Condition Groups, and Assistant Mapping sections with a toggle for each assistant.

5.  Update the **Name**, **Metric type**, or **Description** as needed.

    For a system-provided \(**Out of the box**\) metric, the metric details and condition logic are read-only. You can still update assistant mapping. System-provided metrics are active by default and can't be deactivated.

6.  Update the condition logic in the condition builder as needed.

    Add, remove, or update condition groups, and connect them with AND, OR, or NOT operators. Groups can be nested to form recursive logic. Hover over a column header in the condition builder for a description of that field.

    If the metric is active and mapped to one or more AI assistants, your changes apply to deflection calculations going forward after you save. Deflection rates already calculated under the previous condition logic aren't recalculated.

7.  Select **Test against live data** to validate your changes before saving.

    Select a date and an assistant, then select **Run test**. The results show the number of requests that matched the updated criteria for the selected day \(matching count\), and how many of those requests count as deflected under the updated logic \(deflected count\).

    Testing is especially useful when the metric is already mapped to one or more assistants, so you can confirm your changes produce the expected results before they affect live deflection scoring.

8.  In the **Assistant mapping** section, enable or disable the toggle next to each AI assistant to map or unmap it from this metric.

    Each assistant can be mapped to one metric at a time. Enabling the toggle for an assistant here replaces any metric that assistant was previously mapped to. Disabling the toggle unmaps the assistant from this metric and reassigns it to the system-provided default metric.

9.  Select **Save**.

10. To activate or deactivate the metric, select **Activate** or **Deactivate** and confirm.

    Activate a metric to make it eligible for deflection rate calculations. Deactivate a metric to remove it from scoring. When you deactivate a metric, all assistants mapped to it are remapped to the system-provided default metric. System-provided metrics cannot be deactivated.


## Result

The custom metric reflects your updated condition logic and assistant mapping. If you activated the metric, the deflection rate shown on each mapped assistant's Performance view is calculated using this metric.

**Parent Topic:**[Custom metrics in AI Admin Center \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-admin-center-custom-metric.md)

