---
title: View MISP Feeds
description: View the MISP Feeds that are configured in the base system.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [View Threat Intel Feeds, Threat Intelligence Feeds, Integrate, Threat Intelligence Security Center, Security Operations]
---

# View MISP Feeds

View the MISP Feeds that are configured in the base system.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click on **Integrations** icon.

3.  Select **MISP**.

    The MISP feeds within the base system are described in the following table.

    |Threat Feed|Description|URL|
    |-----------|-----------|---|
    |DigitalSide Threat Intel OSINT Feed|Data source to fetch Open Source Cyber Threat Intelligence information from DigitalSide Threat-Intel OSINT feed, which is mostly based on malware analysis and compromised URLs, IPs and domains.|[https://osint.digitalside.it/Threat-Intel/digitalside-misp-feed/manifest.json](https://osint.digitalside.it/Threat-Intel/digitalside-misp-feed/manifest.json)|
    |URLhaus IOCs|URLhaus is a project from abuse.ch with the goal of sharing malicious URLs that are being used for malware distribution.|[https://urlhaus.abuse.ch/downloads/misp/manifest.json](https://urlhaus.abuse.ch/downloads/misp/manifest.json)|
    |Malware Bazaar|MalwareBazaar is a project from abuse.ch with the goal of sharing malware samples with the infosec community, AV vendors and threat intelligence providers.|[https://bazaar.abuse.ch/downloads/misp/manifest.json](https://bazaar.abuse.ch/downloads/misp/manifest.json)|
    |ThreatFox IOCs|ThreatFox is a free platform from abuse.ch with the goal of sharing indicators of compromise \(IOCs\) associated with malware with the infosec community, AV vendors and threat intelligence providers.|[https://threatfox.abuse.ch/downloads/misp/manifest.json](https://threatfox.abuse.ch/downloads/misp/manifest.json)|

    **Note:** For MISP feed types, the REST endpoint URLs that end with `/manifest.json` are supported.

4.  Click **Edit** to edit the feed.


**Parent Topic:**[View Threat Intel Feeds](../concept/base-system-threat-intel-feeds.md)

