---
title: Usage Insight Data Export release notes
description: Version history for the ServiceNow Usage Insight Data Export application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-air-usage-insight-data-export.html
release: store
topic_type: reference
last_updated: "2026-07-09"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Platform Analytics release notes, ServiceNow Store release notes]
---

# Usage Insight Data Export release notes

Version history for the ServiceNow® Usage Insight Data Export application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.0.1 - July 2026**
    -   Usage Insight Data Export lets you programmatically export your User Experience Analytics \(UXA\) usage data from ServiceNow so you can analyze it alongside data from your other systems. Submit an export request through a simple REST API, and your data is processed asynchronously and delivered in batches to a dedicated, account-isolated messaging topic that you consume with a standard Kafka client.
    -   Select exactly the event fields you need, filter by event name, channel, application, and date range, and move usage data at scale on a recurring schedule. With hashed user identifiers, instance-scoped security, and high-availability delivery, Data Export brings ServiceNow usage insights into your analytics tools for deeper analysis and broader insights by joining your datasets.
    -   What's included:
        -   Programmatic REST API — Submit export requests via a single POST endpoint, secured with mutual SSL authentication and accessed through a dedicated role.
        -   Asynchronous processing — Requests return immediately with a job ID, so large exports run in the background without blocking.
        -   Results delivery via Kafka — Results are streamed in JSON batches to a dedicated Hermes topic you consume with a standard Kafka client.
        -   Flexible column selection — Choose exactly which event fields to export, including name, timestamp, channel, hashed user ID, and application.
        -   Filtering — Narrow exports by event name, channel, application, and date range.
        -   Privacy-preserving — User identifiers are hashed by default.
        -   Built for scale — Run recurring, high-volume exports beyond what manual export supports, with date ranges up to 90 days per request.
-   **Version 1.0.0 - July 2026**

    Usage Insight Data Export lets you programmatically export your User Experience Analytics \(UXA\) usage data from ServiceNow so you can analyze it alongside data from your other systems. Submit an export request through a simple REST API, and your data is processed asynchronously and delivered in batches to a dedicated, account-isolated messaging topic that you consume with a standard Kafka client. Select exactly the event fields you need, filter by event name, channel, application, and date range, and move usage data at scale on a recurring schedule. With hashed user identifiers, instance-scoped security, and high-availability delivery, Data Export brings ServiceNow usage insights into your analytics tools for deeper analysis and getting broader insights by joining your datasets.


**Parent Topic:**[ServiceNow Store - Platform Analytics release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-air.md)

