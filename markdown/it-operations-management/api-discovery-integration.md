---
title: API discovery and synthetic monitoring integration
description: Synthetic Monitoring integrates with API Insights to enable proactive monitoring of discovered APIs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/api-discovery-integration.html
release: australia
topic_type: concept
last_updated: "2026-07-20"
reading_time_minutes: 1
keywords: [synthetic monitoring, API Insights, discovery, integration]
breadcrumb: [Explore, Synthetic monitoring, ITOM AIOps, IT Operations Management]
---

# API discovery and synthetic monitoring integration

Synthetic Monitoring integrates with API Insights to enable proactive monitoring of discovered APIs.

## How the integration works

API Insights discovers APIs across your estate and represents each one in the Configuration Management Database \(CMDB\) as an API component CI. You create a synthetic monitor directly against that existing API component CI — Synthetic Monitoring does not create a new CI.

The integration eliminates manually configuring endpoint details, as the API component CI already captures the endpoint URL and HTTP method. If the API is related to an application service in the CMDB, that relationship is used to populate the monitor's service automatically. Service relationships are optional and may not be present for every discovered API.

## Benefits

-   The API component CI already carries the endpoint URL and HTTP method, so you don't configure them manually
-   Proactive monitoring identifies issues before users are impacted
-   Continuous validation of API availability and performance
-   Integration with existing CMDB relationships and service mapping
-   Consistent monitoring across all discovered APIs

## Workflow

The following workflow describes how API discovery integrates with synthetic monitoring:

1.  API Insights discovers an API endpoint in your environment and represents it in the CMDB as an API component CI.
2.  You create a synthetic monitor directly against that existing API component CI. See [Create a synthetic monitor for a discovered API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/create-synthetic-monitor-for-discovered-api.md).
3.  The monitor continuously tests the API at the specified frequency.
4.  Test results are displayed on the monitor details page.
5.  Alerts are generated when tests fail based on your configured criteria.

## Discovery sources

Synthetic monitors can be created for APIs discovered through the following sources:

-   **API Insights**

    APIs discovered and cataloged through the API Insights application. The application provides visibility into API usage, performance, and dependencies.


