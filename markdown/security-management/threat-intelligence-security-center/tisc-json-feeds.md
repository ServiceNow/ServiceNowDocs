---
title: View JSON Feeds
description: Display all JSON feeds configured in your ServiceNow instance to review their settings and status. Use this to monitor data integration endpoints and troubleshoot feed issues.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [View Threat Intel Feeds, Threat Intelligence Feeds, Integrate, Threat Intelligence Security Center, Security Operations]
---

# View JSON Feeds

Display all JSON feeds configured in your ServiceNow instance to review their settings and status. Use this to monitor data integration endpoints and troubleshoot feed issues.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Select the **Integrations** icon.

3.  Select **JSON** option.

    The configured JSON feeds within the base system appear.

    |Threat Feed|Description|URL|
    |-----------|-----------|---|
    |Feodotracker C&amp;C Hosts|Data source to fetch Botnet C2 IP Blocklist from Feodotracker|[https://feodotracker.abuse.ch/downloads/ipblocklist\_recommended.json](https://feodotracker.abuse.ch/downloads/ipblocklist_recommended.json)|
    |Feodotracker|Data source to fetch Botnet C2 IP Blocklist from Feodotracker|[https://feodotracker.abuse.ch/downloads/ipblocklist.json](https://feodotracker.abuse.ch/downloads/ipblocklist.json)|

4.  Select **Edit** to edit the feed to make the necessary updates.

5.  Select **Save** to apply the changes.


**Parent Topic:**[View Threat Intel Feeds](../concept/base-system-threat-intel-feeds.md)

