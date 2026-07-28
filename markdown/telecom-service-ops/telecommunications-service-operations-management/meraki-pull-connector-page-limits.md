---
title: Page limits for Meraki pull connector endpoints
description: The Meraki pull connector paginates API requests so that all records are retrieved for large organizations. The page size is set per endpoint to match each endpoint's maximum supported value in the Meraki API v1.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/meraki-pull-connector-page-limits.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: reference
last_updated: "2026-07-28"
reading_time_minutes: 1
breadcrumb: [Reference, Telecommunications Service Operations Management]
---

# Page limits for Meraki pull connector endpoints

The Meraki pull connector paginates API requests so that all records are retrieved for large organizations. The page size is set per endpoint to match each endpoint's maximum supported value in the Meraki API v1.

## How pagination works

The connector follows the pagination links returned in the `Link` header \(`rel=next`\) until all pages are consumed, then aggregates the data from every page. The page size is controlled by the `perPage` parameter, which is configured per endpoint as shown in the following table.

|Endpoint|Items per page \(`perPage`\)|
|--------|----------------------------|
|`/organizations`|1000|
|`/organizations/{orgId}/networks`|1000|
|`/organizations/{orgId}/devices`|1000|
|`/organizations/{orgId}/appliance/uplink/statuses`|1000|
|`/organizations/{orgId}/appliance/uplinks/usage/byNetwork`|20|
|`/organizations/{orgId}/appliance/vpn/stats`|300|
|`/organizations/{orgId}/switch/ports/statuses/bySwitch`|20|
|`/organizations/{orgId}/configurationChanges`|1000|

## Endpoints without a page limit

Endpoints that do not have a configured `perPage` limit \(for example, `/devices/{serial}/appliance/performance` and `/networks/{networkId}/appliance/trafficShaping/uplinkBandwidth`\) are treated as single requests. These endpoints return all of their data in one response, so the `Link` header is absent and the pagination loop exits after the first page.

**Parent Topic:**[Telecommunications Service Operations Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/components-installed-with-tsom.md)

