---
title: Pull connector granularity
description: Granularity controls the time resolution of metrics samples collected by a pull connector from the source system API. Aligning granularity with the polling interval reduces API calls to the source system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/pull-connector-granularity.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-07-28"
reading_time_minutes: 1
breadcrumb: [Performance management: Metric collection, Telecom Assurance, Explore, Telecommunications Service Operations Management]
---

# Pull connector granularity

Granularity controls the time resolution of metrics samples collected by a pull connector from the source system API. Aligning granularity with the polling interval reduces API calls to the source system.

Pull connectors for Cisco Meraki and Fortinet use two related timing settings:

-   **Polling interval**

    How often the connector calls the source system API. The default polling interval is 15 minutes.

-   **Granularity**

    The time resolution of each sample returned by the API. A granularity of 5 minutes means each API call returns data in 5-minute increments.


When the polling interval is 15 minutes and the granularity is 5 minutes, each polling cycle retrieves 3 samples, covering the full 15-minute window. Polling every 5 minutes for a single sample results in three times as many API calls for the same data.

Each connector type and API endpoint enforces minimum and maximum values for the granularity and metrics collection schedule fields. The system rejects values outside the supported range when you save the connector instance. For the specific constraints per connector and API type, see [Pull connector granularity constraints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/pull-connector-granularity-constraints.md).

**Related topics**  


[Configure an event pull connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-an-event-pull-connector.md)

[Configure elastic event pull connectors for MPN](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-mpn-connectors-for-events-and-metrics.md)

