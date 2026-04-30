---
title: Add Splunk Enterprise data to Service Observability dashboard templates
description: Add Splunk Enterprise data to charts on Service Observability dashboard templates when you want to view those metrics in context of Service Observability.
locale: en-US
release: zurich
product: Service Observability
classification: service-observability
topic_type: task
last_updated: "2026-02-03"
reading_time_minutes: 2
breadcrumb: [Customize dashboard templates, Configuring Service Observability, Service Observability, ITOM AIOps, IT Operations Management]
---

# Add Splunk Enterprise data to Service Observability dashboard templates

Add Splunk Enterprise data to charts on Service Observability dashboard templates when you want to view those metrics in context of Service Observability.

## About this task

You can add metrics that are stored in Splunk Enterprise to your Service Observability dashboards. These charts display with data from the query you add to the chart.

**Note:** The results from these queries are not automatically scoped to the selected service.

## Before you begin

You need a connection to your Splunk Enterpise instance. See [Connect a Service Observability data source](../task/connect-an-observability-data-source.md) for more information.

Role required: sn\_sow\_svcobs.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace** and then navigate to a service record.

    You can access a service record from these pages in the SOW:

    -   **Services** list: Choose a service from the list.
    -   **Service dashboard**: Choose a service in the dashboard and select **Service Details**.
    -   **List**: Navigate to **Application Services** &gt; **Services** and select a service.
    -   **Express list** alert: Select a service from the **Impacted services** column.
    The Service Details page opens and the Overview tab is displayed.

    If charts are displaying error messages, see [Chart error states](../reference/chart-error-states.md).

2.  Open the template in editing mode.

    -   If you're editing a certified template, select **Duplicate**.
    -   If you're editing a custom template, select **Edit**.
    **Note:** Duplicating a certified template keeps you from overwriting it and also lets you reinstall it.

    The new dashboard is titled with the words `- Copy` appended. Use the pencil icon to change the dashboard name.

3.  To do basic editing, such as rearranging, resizing, or deleting charts, follow the instructions for [Edit in-line Platform Analytics dashboard elements](https://www.servicenow.com/docs/access?context=edit-db-elements-in-ac&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

4.  To add a new chart with MetricBase data, follow these steps:

    1.  In Edit mode, select **Add new element** and choose **Data visualization**, select **New Visualization**, and then select **Line**.

    2.  In the **Data sources** section of the Configuration panel, select **Add data source**.

    3.  In the **Add data source** page, navigate to **Service Observability** &gt; **Splunk Enterprise Metrics**, paste in a query from an existing Splunk chart, and then choose **Add this source**.

        The data is added to the dashboard.

    4.  Use the controls in the **Data** section of the Configuration panel to select the metric and configure the query.

5.  When done customizing, select **Save** and then **Exit editing mode.**

6.  To return the template to the default \(Certified\) version, use the **More actions** menu to select **Return to certified**.


**Parent Topic:**[Customize Service Observability dashboard templates](../task/customize-service-observability-dashboard-templates.md)

