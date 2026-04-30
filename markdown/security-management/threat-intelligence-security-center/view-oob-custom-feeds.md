---
title: View Custom Feed
description: View the custom feed that are shipped within the base system.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [View Threat Intel Feeds, Threat Intelligence Feeds, Integrating Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# View Custom Feed

View the custom feed that are shipped within the base system.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click on **Integrations** icon.

3.  Select **Custom**.

    The following table list out of the box Custom feed.

    |ThreatFeed|Description|URL|
    |----------|-----------|---|
    |CrowdStrike Feed|Source for getting CrowdStrike Actor, Observable and Reports data.|[https://api.crowdstrike.com](https://api.crowdstrike.com)|

4.  Click **Edit** to edit the feed.


-   **[Configure custom CrowdStrike feed](premium-threat-feed-for-crowdstrike.md)**  
The CrowdStrike feed enables users to ingest indicators, actors, reports, and their associated context from the CrowdStrike Falcon Intelligence feed into TISC.
-   **[Configure custom MISP feed](tisc-premium-misp.md)**  
The Malware Information Sharing Platform \(MISP\) API feed enables you to import events from the MISP server, along with their associated attributes and objects, into the TISC library.

**Parent Topic:**[View Threat Intel Feeds](../concept/base-system-threat-intel-feeds.md)

