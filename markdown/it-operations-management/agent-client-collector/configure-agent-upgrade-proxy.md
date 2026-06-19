---
title: Configure a download proxy for Agent Client Collector upgrades
description: Add a proxy server entry so that agents behind a corporate proxy can download upgrade packages from the ServiceNow Content Delivery Network \(CDN\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/configure-agent-upgrade-proxy.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-05-28"
reading_time_minutes: 2
keywords: [ACC upgrade proxy, Package Download Proxies, CDN proxy]
breadcrumb: [Agent Client Collector upgrade overview, ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# Configure a download proxy for Agent Client Collector upgrades

Add a proxy server entry so that agents behind a corporate proxy can download upgrade packages from the ServiceNow Content Delivery Network \(CDN\).

## Before you begin

This configuration applies only to agents connected via Cloud Services \(ICS\) that can't reach the CDN directly. Agents connected via MID Server download packages from the MID Server or the Install Server and don't use this proxy configuration.

Role required: agent\_client\_collector\_admin

## About this task

Proxy configuration is managed through the Package Download Proxies table. When you add, update, or remove a proxy record, the system reads all active entries sorted by the **Order** field, generates a proxy list, and automatically pushes the updated configuration to all agents via MID Server configuration sync. No manual file editing or agent restart is required.

The agent tries each proxy in order, from the lowest **Order** value to the highest. If a proxy fails, the agent moves to the next entry. To configure a direct connection as a fallback, add an entry with the URL set to `direct`.

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Package Download Proxies**.

2.  Select **New**.

3.  Fill in the proxy record fields.

    |Field|Description|
    |-----|-----------|
    |Name|Descriptive label for this proxy entry, for example `US-East Corporate Proxy`.|
    |URL|Proxy address in `host:port` format, for example `proxy.example.com:8080`. Enter `direct` to configure a direct connection with no proxy.|
    |Order|Numeric priority. Lower numbers are tried first. Default is 100.|
    |Active|Selected by default. Clear to disable this entry without deleting it.|
    |Domain|The domain this proxy applies to. Use for domain-separated instances.|

4.  Select **Submit**.

    The system generates an updated proxy list and pushes it to all agents via MID Server configuration sync. Changes take effect without an agent restart.

5.  Add additional proxy entries to configure failover.

    Repeat the preceding steps for each proxy, assigning a higher **Order** value to each successive entry. The agent tries each proxy in order and falls back to the next if the current one fails.


## Proxy with direct connection fallback

The following configuration tries a corporate proxy first. If the proxy is unavailable, the agent connects directly to the CDN.

|Name|URL|Order|Active|
|----|---|-----|------|
|Corporate Proxy|`proxy.example.com:8080`|100|Yes|
|Direct Fallback|`direct`|200|Yes|

## What to do next

To temporarily block all CDN downloads, clear the **Active** check box on all proxy records. With no active entries, the system blocks CDN downloads. This is useful during maintenance windows.

