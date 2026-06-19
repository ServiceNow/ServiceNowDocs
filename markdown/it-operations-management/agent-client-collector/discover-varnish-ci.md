---
title: Enable running of Varnish checks
description: Use application fingerprints to discover the Varnish CI, to enable running Varnish checks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/discover-varnish-ci.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ACC deployment - shared between servers and endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Enable running of Varnish checks

Use application fingerprints to discover the Varnish CI, to enable running Varnish checks.

## Before you begin

Role required: discovery\_admin

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Home**.

2.  Select the **Application Fingerprints** tile.

    The **Application Fingerprints** dashboard appears.

3.  Select the **All Suggested Applications** tile.

4.  On the Application Suggestions page, select the **varnishstat** entry in the **Suggested Group Name** column.

    The varnishstat details appear on the Application Suggestion page.

5.  Select Discover Application.

    Discovery locates an application CI for the varnishstat entry. The CI appears on the Application Fingerprints dashboard in the **Created Applications** section.

    \[Omitted image "app-fingerprints-dash.png"\] Alt text: Created Applications section of Application Fingerprints Dashboard

6.  Run basic Discovery on the host machine.


## Result

The varnishstat CI is discovered and a record is created in the u\_cmdb\_ci\_varnishtat table.

The Varnish policies and checks are available to run.

**Parent Topic:**[Deploying Agent Client Collector on both servers and endpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-shared-deployment.md)

