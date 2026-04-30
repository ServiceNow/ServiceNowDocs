---
title: Customize Service Observability dashboard templates
description: Customize Service Observability dashboard templates when you want to view metrics on the Overview or Observability tabs other than the default charts.
locale: en-US
release: xanadu
product: Service Observability
classification: service-observability
topic_type: task
last_updated: "2025-03-17"
reading_time_minutes: 3
breadcrumb: [Configuring Service Observability, Service Observability, ITOM Health, IT Operations Management]
---

# Customize Service Observability dashboard templates

Customize Service Observability dashboard templates when you want to view metrics on the Overview or Observability tabs other than the default charts.

## About this task

Service Observability dashboards are built using templates specific for each Application Performance Monitor \(APM\) vendor and entity tab. They're built using Platform Analytics, letting you customize templates to meet your business needs. For example, you might want to display metrics from your APM vendor that aren't available by default.

The Service Observability dashboards use APM-specific templates. You can see what each template displays by default from its respective reference topic.

-   [Datadog templates](../reference/datadog-templates.md)
-   [Dynatrace templates](../reference/dynatrace-templates.md)
-   [New Relic templates](../reference/new-relic-templates.md)
-   [New Relic Observability dashboard](../reference/new-relic-observability-tab-for-service-observability.md)

**Note:** When you make a customization, you're changing the template and not the individual service's dashboard. This means that dashboards for any services that also use the same data source are also changed.

When you customize a template, a copy of the original is saved so that you can reimplement it if needed. Default dashboards display a `Certified` tag.

## Before you begin

Role required: sn\_sow\_svcobs.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You can access the Service Details page from these pages in the SOW:

    -   **Services** list: Choose a service from the list.
    -   **Service dashboard**: Choose a service in the dashboard and select **Service Details**.
    -   **List**: Navigate to **Application Services** &gt; **Services** and select a service.
    -   **Express list** alert: Select a service from the **Impacted services** column.
    The Service Details page opens and the Overview tab is displayed.

    If charts are displaying error messages, see [Chart error states](../reference/chart-error-states.md).

2.  Open the template in editing mode.

    -   If you're editing a certified template, select **Duplicate**.
    -   If you're editing a custom template, select **Edit**.
    **Note:** Duplicating a certified template keeps you from overwriting it and also lets you reinstall it, if needed.

    The new dashboard is titled with the words `- Copy` appended. Use the pencil icon to change the dashboard name.

3.  To do basic editing, such as rearranging, resizing, or deleting charts, follow the instructions for [Edit Platform Analytics dashboard elements](https://www.servicenow.com/docs/access?context=edit-db-elements-in-ac&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

4.  To add a query for a new chart, follow these steps:

    1.  In Edit mode, select **Add new element** and choose the data visualization type.

    2.  In the **Add data source** page, navigate to **Service Observability** and select your APM vendor.

        Be sure to select the same APM vendor used on the template you're editing.

    3.  Enter a query in the **Metric** card.

        Use the **Docs** link to refer to the APM documentation for help with creating the query.

    4.  To preview your query, select **Run** and then choose a service and entity.

    5.  When satisfied with your query, select **Add this source** to add the chart to the template.

5.  To edit an existing query, follow these steps.

    1.  In Edit mode, select the chart to edit.

    2.  In the **Data sources** section of the Configuration panel, use the **More actions** menu to select **Edit**.

    3.  In the **Edit data source** page, edit the query in the **Metric** card.

    4.  To preview your query, select a service and an entity and select **Run**.

    5.  When satisfied with your query, select **Apply** to edit the chart on the template.

6.  To return the template to the default \(Certified\) version, choose **Edit** and use the **More actions** menu to select **Return to certified**.


**Parent Topic:**[Configuring Service Observability](../concept/configuring-service-observability.md)

