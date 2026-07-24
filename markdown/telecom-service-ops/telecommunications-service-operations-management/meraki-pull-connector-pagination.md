---
title: Pagination in Meraki pull connector metrics requests
description: The Meraki pull connector handles pagination automatically for metrics API requests, ensuring complete data retrieval for large organizations where API responses are returned in multiple pages.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/meraki-pull-connector-pagination.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-07-23"
reading_time_minutes: 1
breadcrumb: [Performance management: Metric collection, Telecom Assurance, Explore, Telecommunications Service Operations Management]
---

# Pagination in Meraki pull connector metrics requests

The Meraki pull connector handles pagination automatically for metrics API requests, ensuring complete data retrieval for large organizations where API responses are returned in multiple pages.

The Meraki API limits the number of items returned in a single response. In large Meraki organizations with many networks or devices, a single metrics request may not return all available data.

The pull connector now follows pagination links in API responses and issues subsequent requests until all pages are retrieved. This applies to metrics HTTP requests and verifies that data collection is complete regardless of organization size.

No configuration is required to enable this behavior. The connector handles pagination transparently as part of each scheduled metrics collection cycle.

For the page size used by each endpoint, see [Page limits for Meraki pull connector endpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/meraki-pull-connector-page-limits.md).

