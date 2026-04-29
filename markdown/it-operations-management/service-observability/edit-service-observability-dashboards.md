---
title: Edit observability data charts on Service Observability dashboard templates
description: Edit Service Observability dashboard templates to view different observability vendor metrics on the Overview or Observability tabs' charts. Metrics are scoped to the selected service.
locale: en-US
release: australia
product: Service Observability
classification: service-observability
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Customize dashboard templates, Configuring Service Observability, Service Observability, ITOM AIOps, IT Operations Management]
---

# Edit observability data charts on Service Observability dashboard templates

Edit Service Observability dashboard templates to view different observability vendor metrics on the Overview or Observability tabs' charts. Metrics are scoped to the selected service.

## About this task

When you edit or add an observability chart on a dashboard, you use the Edit data source page of Platform Analytics to create a query. You use the built-in query editor for simple metric queries and the Advanced mode to create more substantial queries or to paste a query copied from a chart from your observability vendor instance.

When creating an observability chart, you can use the query builder to create simple queries or use the advanced mode to create more substantial queries.

Use simple queries to return metrics associated with services, hosts, and databases. The returned metrics are aggregated across the time window set by the user.

Use advanced query mode to cut and paste queries from existing observability charts into Service Observability. For most observability vendors, you can simply copy a query from an existing chart in your observability instance.

Both query types support [template variables](../reference/service-observability-template-variables.md) that let you use the same query to return metrics for multiple entity instances.

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

3.  To do basic editing, such as rearranging, resizing, or deleting charts, follow the instructions for [Edit in-line Platform Analytics dashboard elements](https://www.servicenow.com/docs/access?context=edit-db-elements-in-ac&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

4.  To add a vendor query for a new chart, follow these steps:

    1.  In Edit mode, select **Add new element** and choose **Data visualization** &gt; **New visualization**.

    2.  In the **Configuration panel**, select `Line` for **Visualization type** and choose **Add data source**.

    3.  In the **Add data source** page, open **Service Observability** in the navigation panel and select your observability vendor.

        Be sure to select the same vendor used on the template you're editing.

    4.  Enter a query in the **Metric** card.

        Use the query builder to edit a simple vendor-specific query.

        To copy a full query from your vendor chart, activate the **Advanced** switch and paste in a query from your vendor chart.

        For AWS and Azure, instead of entering a query in advanced mode, you can import selected charts from an existing dashboard. Select **Import from AWS/Azure Dashboard**. Select a data source name, then select a dashboard and from the list of charts, select the one to import, then select **Import query**. The query for the chart is pasted into the Query box.

        Use [template variables](../reference/service-observability-template-variables.md) to replace any hard-coded entities or time periods to have the query return results that match both the service and time period selected in the UI.

        **Note:** Use the **Docs** link to refer to the vendor-specific documentation for help with creating the query.

    5.  To preview your query, select **Run** and then choose a service and entity.

    6.  When satisfied with your query, select **Add this source** to add the chart to the template.

5.  To edit an existing query, follow these steps.

    1.  In Edit mode, select the chart to edit.

    2.  In the **Data sources** section of the Configuration panel, use the **More actions** menu to select **Edit**.

    3.  In the **Edit data source** page, edit the query in the **Metric** card.

        Use the query builder to create a simple vendor-specific query.

        To copy a full query from your vendor chart, activate the **Advanced** switch and paste in a query from your vendor chart.

        For AWS and Azure, instead of entering a query in advanced mode, you can import selected charts from an existing dashboard. Select **Import from AWS/Azure Dashboard**. Select a data source name, then select a dashboard and from the list of charts, select the one to import, then select **Import query**. The query for the chart is pasted into the Query box.

        Use [template variables](../reference/service-observability-template-variables.md) to replace any hard-coded entities or time periods.

        **Note:** Use the **Docs** link to refer to the vendor-specific documentation for help with creating the query.

    4.  To preview your query, select a service and an entity and select **Run**.

    5.  When satisfied with your query, select **Apply** to add the chart to the template.

6.  When done customizing, select **Save** and then **Exit editing mode.**

7.  To return the template to the default \(Certified\) version, use the **More actions** menu to select **Return to certified**.


**Parent Topic:**[Customize Service Observability dashboard templates](customize-service-observability-dashboard-templates.md)

