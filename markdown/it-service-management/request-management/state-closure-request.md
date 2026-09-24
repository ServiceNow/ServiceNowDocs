---
title: State closure in the request fulfillment execution plan
description: The state closure in the request fulfillment process of a catalog item depends on the status of the associated catalog tasks, request items, and the request. It is applicable only for execution flows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/request-management/state-closure-request.html
release: brazil
product: Request Management
classification: request-management
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Service Catalog request fulfillment, Configure, Request Management, IT Service Management]
---

# State closure in the request fulfillment execution plan

The state closure in the request fulfillment process of a catalog item depends on the status of the associated catalog tasks, request items, and the request. It is applicable only for execution flows.

## State closure dependency between a catalog task and RITM

-   If all catalog tasks are closed as **Closed Complete**, the RITM is closed as **Closed Complete**.
-   If there is at least one catalog task closed as **Closed Incomplete**, the RITM is closed as **Closed Incomplete**.
-   If all catalog tasks are closed as **Closed Skipped**, the RITM is closed as **Closed Skipped**.

## State closure dependency between a RITM and request

-   If all RITMs are closed as **Closed Complete**, the request is closed as **Closed Complete**.
-   If there is at least one RITM closed as **Closed Incomplete**, the request is closed as **Closed Incomplete**.
-   If all RITMs are closed as **Closed Skipped**, the request is closed as **Closed Skipped**.

**Parent Topic:**[Service Catalog request fulfillment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/request-management/request-fulfillment.md)

