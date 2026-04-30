---
title: Dynatrace advanced settings fields
description: Populate the pull connector advanced settings fields to optimize event retrieval and synchronization based on specific requirements such as connection preferences, event frequency, and time zone settings.
locale: en-US
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: reference
last_updated: "2025-10-29"
reading_time_minutes: 1
breadcrumb: [Service Operations Workspace for ITOM reference, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Dynatrace advanced settings fields

Populate the pull connector advanced settings fields to optimize event retrieval and synchronization based on specific requirements such as connection preferences, event frequency, and time zone settings.

<table id="table_cwg_vzv_mbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base API path

</td><td>

Root URL or endpoint used to connect to the Dynatrace Metrics API. All API requests are made relative to this base path.

</td></tr><tr><td>

Initial sync in mins

</td><td>

Time, in minutes, that the system takes to complete the first synchronization of data with the Dynatrace Metrics API.For example, if the value is 15, the connector fetches metrics from the past 15 minutes.

Default: 15

</td></tr><tr><td>

Max metrics per query

</td><td>

Maximum number of metrics that can be requested in a single query to the Dynatrace Metrics API. The value cannot exceed 32, the maximum limit allowed by Dynatrace. Requests exceeding this limit must be split into multiple queries.Default: 32

</td></tr><tr><td>

Page Size

</td><td>

Number of records returned in a single response when querying the Dynatrace Metrics API. If the total results exceed this number, multiple pages are returned.Default: 500

</td></tr><tr><td>

Port

</td><td>

Port number used for connecting to the Dynatrace server.

</td></tr><tr><td>

Request per minute

</td><td>

Maximum number of API requests that can be sent to the Dynatrace Metrics API within one minute. Exceeding this limit may result in throttling or temporary blocking of requests.**Note:** Relevant only when you enable **Throttle API calls**.

Default: 1000

</td></tr><tr><td>

Throttle API calls

</td><td>

Limits the rate of API requests to the Dynatrace Metrics API, preventing overload, request failures, or temporary blocking.Enable this option to automatically limit the rate of API requests, preventing overloading the Dynatrace Metrics API and avoiding request failures.

Default: false

</td></tr><tr><td>

Protocol

</td><td>

Communication protocol used for retrieving events from Dynatrace server.Default: https

</td></tr><tr><td>

Debugging

</td><td>

-   Debug: Provides detailed logs for troubleshooting.
-   Log payload: Displays raw log data. Use only for debugging, as it can quickly fill the MID Server logs.

</td></tr></tbody>
</table>To return to the procedure, see [Configure Dynatrace metric pull connector](../task/configure-dynatrace-metric-pull-connector.md).

**Parent Topic:**[Service Operations Workspace for ITOM reference](../concept/sow-reference-itom.md)

