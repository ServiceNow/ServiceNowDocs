---
title: Customize Service Observability dashboard templates
description: You can customize the Service Observability dashboards on both the Overview and Observability tabs of the Service Details page. You can change or add metrics and related data to fit your business needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-observability/customize-service-observability-dashboard-templates.html
release: australia
product: Service Observability
classification: service-observability
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring Service Observability, Service Observability, ITOM AIOps, IT Operations Management]
---

# Customize Service Observability dashboard templates

You can customize the Service Observability dashboards on both the Overview and Observability tabs of the Service Details page. You can change or add metrics and related data to fit your business needs.

Service Observability dashboards are built using templates specific for each observability vendor and entity tab. They're built using Platform Analytics, letting you customize templates to meet your business needs. For example, you might want to display metrics from your observability vendor that aren't available by default.

The Service Observability dashboards use vendor-specific templates. You can see what each template displays by default from its respective reference topic.

-   [Amazon CloudWatch templates for Service Observability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/aws-templates.md)
-   [AppDynamics templates for Service Observability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/appd-templates.md)
-   [Azure Monitor templates for Service Observability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/azure-templates.md)
-   [Cisco ThousandEyes templates for Service Observability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/cisco-thousand-eyes-templates-for-service-observability.md)
-   [Datadog templates for Service Observability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/datadog-templates.md)
-   [Dynatrace templates for Service Observability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/dynatrace-templates.md)
-   [LogicMonitor templates for Service Observability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/logic-monitor-templates.md)
-   [New Relic templates for Service Observability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/new-relic-templates.md)
-   [Prometheus templates for Service Observability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/prometheus-templates.md)
-   [SolarWinds templates for Service Observability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/solarwinds-templates.md)
-   [Splunk Observability templates for Service Observability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/splunk-templates.md)
-   [Zabbix templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/zabbix-templates.md)

**Note:** When you make a customization, you're changing the template and not the individual service's dashboard. This means that dashboards for any services that also use the same data source are also changed.

Along with observability data, you can also add charts for data from ServiceNow tables and also from data stored in the MetricBase and Health Log Analytics applications.

When you customize a template, a copy of the original is saved so that you can reimplement it if needed. Default dashboards display a `Certified` tag.

-   **[Edit observability data charts on Service Observability dashboard templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/edit-service-observability-dashboards.md)**  
Edit Service Observability dashboard templates to view different observability vendor metrics on the Overview or Observability tabs' charts. Metrics are scoped to the selected service.
-   **[Edit ServiceNow data on Service Observability dashboard templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/edit-sn-based-charts.md)**  
Edit Service Observability dashboard templates to view data from problem and business app records on the Overview or Observability dashboards.
-   **[Add MetricBase charts to Service Observability dashboard templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/add-metric-base-charts.md)**  
Add MetricBase data to charts on Service Observability dashboard templates when you want to view those metrics in context of Service Observability.
-   **[Add Health Log Analytics data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/display-hla-data-on-a-dashboard.md)**  
Add a graph showing logs from Health Log Analytics \(HLA\) in a Service Observability dashboard.
-   **[Add Splunk Enterprise data to Service Observability dashboard templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/add-splunk-enterprise-data.md)**  
Add Splunk Enterprise data to charts on Service Observability dashboard templates when you want to view those metrics in context of Service Observability.

**Parent Topic:**[Configuring Service Observability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/configuring-service-observability.md)

