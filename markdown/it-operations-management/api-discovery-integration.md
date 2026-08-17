---
title: API Insights and synthetic monitoring integration
description: Synthetic Monitoring integrates with API Insights to enable proactive monitoring of discovered APIs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/api-discovery-integration.html
release: zurich
topic_type: concept
last_updated: "2026-07-24"
reading_time_minutes: 1
keywords: [synthetic monitoring, API Insights, discovery, integration]
breadcrumb: [Explore, Landing page, ITOM AIOps, IT Operations Management]
---

# API Insights and synthetic monitoring integration

Synthetic Monitoring integrates with API Insights to enable proactive monitoring of discovered APIs.

## How the integration works

API Insights discovers APIs across your estate through Service Graph Connectors and represents each one in the Configuration Management Database \(CMDB\) as an API component \(cmdb\_ci\_api\_component\) CI. Create a synthetic monitor directly against an existing API component CI to continuously test the availability and performance of the discovered API.

The integration eliminates manually configuring endpoint details. The API component CI already carries the endpoint URL and HTTP method. If the API is related to an application service in the CMDB, that relationship is used to populate the monitor's service automatically.

## Benefits

Integrating API Insights with synthetic monitoring provides the following advantages:

-   Proactive monitoring identifies issues before affecting users
-   Continuous validation of API availability and performance
-   Integration with existing CMDB service relationships when present
-   Consistent monitoring across all discovered APIs

## Workflow

This following workflow describes how API Insights integrates with synthetic monitoring:

1.  API Insights discovers APIs in your environment through Service Graph Connectors and creates API Component CIs in the CMDB.
2.  Creates a synthetic monitor that references the existing API component CI. See [Create a synthetic monitor for a discovered API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/create-synthetic-monitor-for-discovered-api.md).
3.  Tests the API at the specified frequency continuously
4.  Displays the test results on the monitor details page.
5.  Generates alerts when tests fail based on configured criteria.

