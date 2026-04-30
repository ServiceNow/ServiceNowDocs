---
title: Customize Service Observability dashboard templates
description: You can customize the Service Observability dashboards on both the Overview and Observability tabs of the Service Details page. You can change or add metrics and related data to fit your business needs.
locale: en-US
release: yokohama
product: Service Observability
classification: service-observability
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configuring Service Observability, Service Observability, ITOM AIOps, IT Operations Management]
---

# Customize Service Observability dashboard templates

You can customize the Service Observability dashboards on both the Overview and Observability tabs of the Service Details page. You can change or add metrics and related data to fit your business needs.

Service Observability dashboards are built using templates specific for each Application Performance Monitor \(APM\) vendor and entity tab. They're built using Platform Analytics, letting you customize templates to meet your business needs. For example, you might want to display metrics from your APM vendor that aren't available by default.

The Service Observability dashboards use APM-specific templates. You can see what each template displays by default from its respective reference topic.

-   [Amazon CloudWatch templates for Service Observability](../reference/aws-templates.md)
-   [AppDynamics templates for Service Observability](../reference/appd-templates.md)
-   [Azure Monitor templates for Service Observability](../reference/azure-templates.md)
-   [Datadog templates for Service Observability](../reference/datadog-templates.md)
-   [Dynatrace templates for Service Observability](../reference/dynatrace-templates.md)
-   [New Relic templates for Service Observability](../reference/new-relic-templates.md)
-   [Prometheus templates for Service Observability](../reference/prometheus-templates.md)
-   [SolarWinds templates for Service Observability](../reference/solarwinds-templates.md)
-   [Splunk templates for Service Observability](../reference/splunk-templates.md)

**Note:** When you make a customization, you're changing the template and not the individual service's dashboard. This means that dashboards for any services that also use the same data source are also changed.

Along with APM data, you can also add charts for data from ServiceNow tables and also from data stored in the MetricBase and Health Log Analytics applications.

When you customize a template, a copy of the original is saved so that you can reimplement it if needed. Default dashboards display a `Certified` tag.

## Creating APM queries for a chart

When you edit or add a chart on a dashboard, you use the Edit data source page of Platform Analytics to create a query. You use the built-in query editor for simple metric queries and the Advanced mode to paste a query copied from a chart in your APM vendor instance.

Service Observability dashboards are scoped to the service currently displayed in the Service Details page. If you want to use a single query for multiple services and entities and any time range, you can replace hard-coded values with Service Observability [template variables](../reference/service-observability-template-variables.md).

## Add ServiceNow Tables

You can include data from ServiceNow problem records and business application records to dashboards and the data is scoped to the selected service.

## Add MetricBase data charts

You can add charts based on data stored in the MetricBase application. The data is scoped to the selected service.

## Add Health Log Analytics data charts

You can add charts based on data stored in the Health Log Analytics application. The data is scoped to the selected service.

-   **[Edit APM data charts on Service Observability dashboard templates](edit-service-observability-dashboards.md)**  
Edit Service Observability dashboard templates to view different APM vendor metrics on the Overview or Observability tabs' charts.
-   **[Edit ServiceNow data on Service Observability dashboard templates](edit-sn-based-charts.md)**  
Edit Service Observability dashboard templates to view data from problem and business app records on the Overview or Observability dashboards.
-   **[Add MetricBase charts to Service Observability dashboard templates](add-metric-base-charts.md)**  
Add MetricBase data to charts on Service Observability dashboard templates when you want to view those metrics in context of Service Observability.
-   **[Add Health Log Analytics data](../concept/display-hla-data-on-a-dashboard.md)**  
Add a graph showing logs from Health Log Analytics \(HLA\) in a Service Observability dashboard.

**Parent Topic:**[Configuring Service Observability](../concept/configuring-service-observability.md)

