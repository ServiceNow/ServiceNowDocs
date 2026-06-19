---
title: Use synthetic monitoring with Service Observability
description: Create a synthetic monitor to test your service's endpoints. Then display the results by customizing a Service Observability dashboard.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-observability/use-synthetic-monitoring-with-service-observability.html
release: australia
product: Service Observability
classification: service-observability
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customize dashboard templates, Configuring Service Observability, Service Observability, ITOM AIOps, IT Operations Management]
---

# Use synthetic monitoring with Service Observability

Create a synthetic monitor to test your service's endpoints. Then display the results by customizing a Service Observability dashboard.

## Overview of using synthetic monitoring with Service Observability

Synthetic monitoring simulates user transactions on a service's HTTP endpoints, enabling you to identify performance bottlenecks, help confirm up-time, and optimize user experiences. It continually calls a service's endpoint to test availability, response times, or the presence of a defined string in the response body. When a test fails the configured criteria, it can send an alert. For more information about synthetic monitoring, see [Exploring synthetic monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/exploring-synthetic-monitoring.md).

The results of the monitor's test can be added to the Service Observability Overview dashboard and to the Observability Service dashboard. To view synthetic data related to a service on a dashboard, you first create a monitor that tests the endpoints of your service. Then you customize a dashboard template to add the monitor's test results.

**Note:** When you customize the template to add synthetic monitoring, you're adding it to all dashboards that use that template. Services that don't have a configured monitor display an empty chart.

1.  [Create a synthetic monitor to test a service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/create-a-synthetic-monitor-to-test-a-service.md).

    Install and configure synthetic monitoring and then create a monitor to continually test your service's endpoints using status code, response time, or response body as criteria.

2.  [Add synthetic monitor results to a Service Observability dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/add-synthetic-monitor-results-to-a-service-observability-dashboard.md)

    Customize a Service Observability dashboard template to add synthetic monitoring test results.


