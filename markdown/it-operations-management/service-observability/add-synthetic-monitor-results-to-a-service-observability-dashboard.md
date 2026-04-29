---
title: Add synthetic monitor results to a Service Observability dashboard
description: Add a synthetic monitor to a dashboard in Service Observability by customizing an existing dashboard template.
locale: en-US
release: australia
product: Service Observability
classification: service-observability
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use synthetic monitoring with Service Observability, Customize dashboard templates, Configuring Service Observability, Service Observability, ITOM AIOps, IT Operations Management]
---

# Add synthetic monitor results to a Service Observability dashboard

Add a synthetic monitor to a dashboard in Service Observability by customizing an existing dashboard template.

## About this task

Once you have created monitors for your services, you can display those results on your Service Observability dashboards by customizing the template to include a chart that queries synthetic monitoring. You can add synthetic monitoring to either the Overview dashboard or the Observability &gt; Service dashboard.

**Note:** When you customize the template to add synthetic monitoring, you're adding it to all dashboards that use that template. Services that don't have a configured monitor display an empty chart.

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

3.  To add a new ServiceNow table, follow these steps:

    1.  In Edit mode, select **Add new element** and choose **List**.

    2.  In the **Configuration panel** in the **Data sources** section, choose **Add data source**.

    3.  In the **Add data source** page, search for and select the synthetic monitoring data source, depending on the data you want to display.

    -   If you want to display the status of all tests associated with a service, select the `Single API` \[sn\_synthetics\_check\_single\_api\] table.
    -   If you want to display the results of a single synthetic test for a service, select the `Single API Result` \[sn\_synthetics\_check\_single\_api\_result\] table.
    **Note:** Leave the **Follow filters** check box selected. This control enables the chart to display information for the selected service.

4.  In the **Default display** section, choose **Add** to begin adding columns from the table to the new list.

5.  Choose **Save** and then **Exit editing mode** to return to the dashboard.

    The synthetic monitoring data now appears on the dashboard.


## What to do next

For detailed instructions about editing dashboards, see [Edit in-line Platform Analytics dashboard elements](https://www.servicenow.com/docs/access?context=edit-db-elements-in-ac&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

**Parent Topic:**[Use synthetic monitoring with Service Observability](use-synthetic-monitoring-with-service-observability.md)

