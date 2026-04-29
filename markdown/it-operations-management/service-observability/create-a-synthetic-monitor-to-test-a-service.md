---
title: Create a synthetic monitor to test a service
description: Install and configure synthetic monitoring and then create a monitor for your service.
locale: en-US
release: australia
product: Service Observability
classification: service-observability
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use synthetic monitoring with Service Observability, Customize dashboard templates, Configuring Service Observability, Service Observability, ITOM AIOps, IT Operations Management]
---

# Create a synthetic monitor to test a service

Install and configure synthetic monitoring and then create a monitor for your service.

## Before you begin

Your service must have an HTTP-reachable endpoint, configured as a CI in the HTTP\(S\) Endpoints \[cmdb\_ci\_endpoint\_http\] table of the Configuration Management Database \(CMDB\).

Role required: n\_sow\_svcobs.admin, sn\_sow\_synthetics.synthetics\_admin

## Procedure

1.  Install synthetic monitoring.

    See [Install synthetic monitoring](../../synthetic-monitoring/task/install-synthetic-monitoring.md) for more information.

2.  If needed, create a location to run the monitor from.

    Monitors can be run locally from a ServiceNow Glide instance or from your environment using either a cluster of Agent Client Collector \(ACC\) agents or from a MID Server. If you choose to run them from your environment, you must create a location. See [Create synthetic monitoring locations](../../synthetic-monitoring/task/create-synthetic-monitoring-locations.md) for more information.

3.  Create the monitor.

    Follow the steps in [Create and edit a synthetic monitor](../../synthetic-monitoring/task/create-synthetic-monitor.md). Be sure to select the service you want to monitor as the **Related service CI**.


## What to do next

Once you create the monitor, it begins running tests. View the results of those tests to verify the results before embedding synthetic monitoring into a Service Observability dashboard. For more information about viewing monitor test results, see [Identifying system issues with synthetic monitoring](../../synthetic-monitoring/concept/identifying-system-issues.md).

Once you have expected results, move on to [Add synthetic monitor results to a Service Observability dashboard](add-synthetic-monitor-results-to-a-service-observability-dashboard.md).

**Parent Topic:**[Use synthetic monitoring with Service Observability](use-synthetic-monitoring-with-service-observability.md)

