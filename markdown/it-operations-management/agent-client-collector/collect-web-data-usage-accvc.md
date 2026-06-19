---
title: Collect web usage data using Agent Client Collector for Visibility - Content
description: Track website visits across your organization and gain visibility into web applications your users access using Agent Client Collector for Visibility - Content \(ACC-VC\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/collect-web-data-usage-accvc.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-25"
reading_time_minutes: 2
keywords: [ACC-V, web usage, monitoring, visibility content]
breadcrumb: [ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Collect web usage data using Agent Client Collector for Visibility - Content

Track website visits across your organization and gain visibility into web applications your users access using Agent Client Collector for Visibility - Content \(ACC-VC\).

## Before you begin

Verify that the following components are installed in your environment:

-   Agent Client Collector Framework \(ACC-F\)
-   Agent Client Collector for Visibility - Content
-   URL Discovery and Monitoring \(sn\_itom\_url\_disc\)
-   The DEX Browser Extension 4.1.0 is enabled on the host

Role required: sn\_acc\_vis\_content.application\_admin and discovery\_admin

## About this task

Web data collection is enabled on Windows and macOS platforms.

Web data collection is supported on Chromium and Edge browsers.

ACC-VC can collect web usage data in the following modes:

-   Configured monitoring \(tracks only pre-configured websites\)
-   Full monitoring \(captures domain-level website access activity from supported Chromium-based browsers on managed corporate devices\). Automatically captures domain-level usage data from managed Windows and macOS devices and stores it in the User Web Usage \(sn\_acc\_vis\_content\_user\_web\_usage\) table.

For details on URL Discovery, see [URL Discovery Insights dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/url-disco-insights.md) and [Discovery Admin Workspace Settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/discovery-admin-workspace-setup.md).

## Procedure

1.  Navigate to **System Definition** &gt; **System Properties**.

2.  Search for the property **sn\_acc\_vis\_content.enable\_full\_monitoring**.

3.  Set the **Value** field to `true`.

    Setting this property to true automatically activates the VISC Get URL Metrics monitoring policy and enables full monitoring of web usage data for all websites visited on Chromium-based browsers. Setting it to false deactivates the policy.

4.  Select **Update**.

    The system activates the VISC Get URL Metrics monitoring policy and begins collecting web usage data from managed devices.

5.  Configure the data retention period by searching for the property **sn\_acc\_vis\_content.web\_usage\_retention\_days** and setting the desired number of days.

    The default retention period is 7 days. Records older than this value are automatically deleted. Modifying this value updates the auto-flush retention period for the User Web Usage \(sn\_acc\_vis\_content\_user\_web\_usage\) and Application Domain \(sn\_acc\_vis\_content\_application\_domain\) tables.


## Result

The ACC agent on each managed device monitors URL activity from Chromium-based browsers and stores the data locally. At scheduled intervals \(default: once every 24 hours\), the agent runs the VISC Get URL Metrics check and sends the data to your instance. The data is processed and stored in the User Web Usage table, with daily aggregation jobs updating domain-level totals. For details on the VISC Get URL Metrics policy and check, see [Agent Client Collector for Visibility - Content default checks and policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-visibility-checks-policies.md).

## What to do next

After enabling web usage collection, you can view the collected data in the User Web Usage \(sn\_acc\_vis\_content\_user\_web\_usage\) table and monitor aggregated domain-level statistics in the Application Domain \(sn\_acc\_vis\_content\_application\_domain\) table. Data aggregates from the User Web Usage table to the Application Domain table, including total page views, total unique users, last accessed time, and daily page view trends. By default, this job runs daily.

For details on these tables, see [Web usage data collection tables and fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/web-usage-collection-tables.md).

**Parent Topic:**[Deploying Agent Client Collector on servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-server-deployment.md)

