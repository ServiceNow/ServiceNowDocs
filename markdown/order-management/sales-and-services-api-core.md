---
title: Sales and Service API Core
description: Enables seamless tracking and management of Sales Customer Relationship Management workflows through structured inbound and outbound request handling, configurable flow processing, and integration with external systems.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Sales and Service API Core

Enables seamless tracking and management of Sales Customer Relationship Management workflows through structured inbound and outbound request handling, configurable flow processing, and integration with external systems.

## Overview of Sales and Service API Core

The Sales and Service API Core \(com.sn\_tmt\_core\) plugin has three key components.

<table id="table_t1y_j4g_xgc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Inbound Request](som_request_tracker.md) \(sn\_tmt\_core\_inbound\_queue\)

</td><td>

Tracks the status of both synchronous and asynchronous flows. It enables agents to monitor the progress of requests and also enables sequential processing of dependent records to maintain data accuracy and consistency.

 It captures detailed status information for each request. For example, when an order is created from a quote, it logs a confirmation message with the order header number.

 It also supports archival and cleanup policies enabling organizations to cleanup records by applying different durations for successful and failed requests to optimize data management.

</td></tr><tr><td>

[Inbound Request Configuration](inbound-request-configuration-table.md) \(sn\_tmt\_core\_inbound\_queue\_config\)

</td><td>

Defines how each flow is processed and tracked.

 It’s a metadata table that is referenced by the Request Configuration field in the Inbound Request Table.

 It enables administrators to:

-   Configure synchronous vs asynchronous processing.
-   Adapt the Request Tracker across CRM flows.
-   Set notification types \(default, custom, or none\).

</td></tr><tr><td>

[Outbound Request](outbound-request-configuration-table.md) \(sn\_tmt\_core\_outbound\_request\)

</td><td>

Facilitates outbound interactions with external Service Order Management \(SOM\).

 It supports end-to-end order fulfillment via bi-directional REST API integration and requires specific roles.

</td></tr></tbody>
</table>|Role|Access|
|----|------|
|sn\_tmt\_core.admin|Create, read, update, delete, report\_view, and report\_on|
|sn\_tmt\_core.viewer|report\_view, report\_on, and read|

