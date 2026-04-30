---
title: Add Health Log Analytics data
description: Add a graph showing logs from Health Log Analytics \(HLA\) in a Service Observability dashboard.
locale: en-US
release: yokohama
product: Service Observability
classification: service-observability
topic_type: task
last_updated: "2025-11-04"
reading_time_minutes: 2
breadcrumb: [Customize dashboard templates, Configuring Service Observability, Service Observability, ITOM AIOps, IT Operations Management]
---

# Add Health Log Analytics data

Add a graph showing logs from Health Log Analytics \(HLA\) in a Service Observability dashboard.

## About this task

You can add logs from [HLA](../../health-log-analytics-admin/reference/hla-landing-page.md) to your Service Observability dashboards. These charts display with data scoped to the selected service.

## Before you begin

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

3.  To do basic editing, such as rearranging, resizing, or deleting charts, follow the instructions for [Edit Platform Analytics dashboard elements](https://www.servicenow.com/docs/access?context=edit-db-elements-in-ac&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

4.  To add a new chart with HLA data, follow these steps:

    1.  In Edit mode, select **Add new element** and choose **Data visualization**, select **New Visualization**, and then select **Line**.

    2.  In the **Data sources** section of the Configuration panel, select **Add data source**.

    3.  In the **Add data source** page, navigate to **Health Log Analytics** &gt; **Log components**.

    4.  Enter a saved search or select a component and then optionally add conditions or a Lucene query, as described in Step 5 of [Create log data dashboards and visualizations](../../health-log-analytics-admin/task/hla-log-data-dashboard-create.md).

    5.  Once the filter is correct, choose **Add this source**.

        The data is added to the dashboard.

    6.  Use the controls in the **Data** section of the Configuration panel to further configure the chart.

5.  When done customizing, select **Save** and then **Exit editing mode.**

6.  To return the template to the default \(Certified\) version, use the **More actions** menu to select **Return to certified**.


**Parent Topic:**[Customize Service Observability dashboard templates](../task/customize-service-observability-dashboard-templates.md)

