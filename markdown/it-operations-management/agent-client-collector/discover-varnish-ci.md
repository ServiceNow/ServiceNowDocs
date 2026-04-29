---
title: Enable running of Varnish checks
description: Use application fingerprints to discover the Varnish CI, to enable running Varnish checks.
locale: en-US
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

    ![Created Applications section of Application Fingerprints Dashboard](../image/app-fingerprints-dash.png "Created applications section of Application Fingerprints dashboard")

6.  Run basic Discovery on the host machine.


## Result

The varnishstat CI is discovered and a record is created in the u\_cmdb\_ci\_varnishtat table.

The Varnish policies and checks are available to run.

**Parent Topic:**[Deploying Agent Client Collector on both servers and endpoints](../concept/acc-shared-deployment.md)

