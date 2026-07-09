---
title: Create and manage MetricBase data mappings
description: Map your services to metrics from MetricBase, and view them in charts for the service.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-observability/create-and-manage-metricbase-data-mappings.html
release: australia
product: Service Observability
classification: service-observability
topic_type: task
last_updated: "2026-06-12"
reading_time_minutes: 2
breadcrumb: [Configuring Service Observability, Service Observability, ITOM AIOps, IT Operations Management]
---

# Create and manage MetricBase data mappings

Map your services to metrics from MetricBase, and view them in charts for the service.

## Before you begin

-   You can map any of the following service types:
    -   Service instance
    -   Mapped application service
    -   Calculated application service
    -   Dynamic CI group
    -   Technology management service
    -   Tag-based service
    -   Offerings
    -   Business service
-   Your instance has metrics in MetricBase.

Role required: sn\_sow\_svcobs.admin

## About this task

When a service CI is mapped to MetricBase, Service Observability can display metrics from MetricBase for that service and its related entities \(such as hosts, databases, and network devices\). The system automatically identifies the entities through CMDB relationships.

When you select MetricBase as your data source, generic dashboards appear that display ServiceNow-native charts. You can customize these dashboards by adding MetricBase charts for the specific metrics you want to view. See [Add MetricBase charts to Service Observability dashboard templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/add-metric-base-charts.md) for more information.

## Procedure

1.  Navigate to **All** &gt; **Service Observability** &gt; **Configure Data mappings**.

2.  Select **Create your first mapping** or **Create mapping**.

3.  On the Observability data mapping page, enter a name for the mapping.

4.  Choose the services that should use this mapping.

    1.  Choose **Select services**.
    2.  Use the navigation to narrow down the list to the type of service you're searching for.
    3.  Select the services to add to the mapping. You can add services from any combination of service type.

        **Note:** Use the filter to narrow down the service list.

    4.  Select **Add services** to add them to the mapping.
    The Mapping preview pane updates to show the selected service, or the first service in a list of services.

5.  Select **MetricBase** as the data source for this mapping.

    Service Observability automatically detects and displays the entities related to your services. No additional configuration is required.

6.  If some of your entities require different configurations, create exceptions to the default policy by configuring them in the Exceptions card.

7.  Test the mapping.

    The **Mapping preview** panel shows the test results for the first service mapped. Service Observability sends a request and returns the entities found using the provided mapping. If the results don't seem correct, try reconfiguring the mapping or adjusting your exception rules.

    If you have more than one service mapped, use the **Service** drop-down menu to select and test a different service.

8.  Select **Save mapping**.


## Result

On the **Observability** tab of the Service details page, dashboards for the selected service\(s\) show ServiceNow-native charts. You can customize these dashboards by adding MetricBase charts for the specific metrics you want to view. See [Add MetricBase charts to Service Observability dashboard templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/add-metric-base-charts.md) for more information.

**Parent Topic:**[Configuring Service Observability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/configuring-service-observability.md)

