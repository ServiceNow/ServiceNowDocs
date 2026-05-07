---
title: View MISP Feeds
description: View configured MISP feeds to monitor threat intelligence sources and verify feed status in your ServiceNow instance.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [View Threat Intel Feeds, Threat Intelligence Feeds, Integrate, Threat Intelligence Security Center, Security Operations]
---

# View MISP Feeds

View configured MISP feeds to monitor threat intelligence sources and verify feed status in your ServiceNow instance.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Select the **Integrations** icon.

3.  Select **MISP**.

    The MISP feeds within the base system are described in this table.

    |Threat Feed|Description|URL|
    |-----------|-----------|---|
    |DigitalSide Threat Intel OSINT Feed|Data source to fetch Open Source Cyberthreat Intelligence information from DigitalSide Threat-Intel OSINT feed, which is mostly based on malware analysis and compromised URLs, IPs and domains.|[https://osint.digitalside.it/Threat-Intel/digitalside-misp-feed/manifest.json](https://osint.digitalside.it/Threat-Intel/digitalside-misp-feed/manifest.json)|
    |URLhaus IOCs|URLhaus is a project from abuse.ch with the goal of sharing malicious URLs that are being used for malware distribution.|[https://urlhaus.abuse.ch/downloads/misp/manifest.json](https://urlhaus.abuse.ch/downloads/misp/manifest.json)|
    |Malware Bazaar|MalwareBazaar is a project from abuse.ch with the goal of sharing malware samples with the infosec community, AV vendors and threat intelligence providers.|[https://bazaar.abuse.ch/downloads/misp/manifest.json](https://bazaar.abuse.ch/downloads/misp/manifest.json)|
    |ThreatFox IOCs|ThreatFox is a free platform from abuse.ch with the goal of sharing indicators of compromise \(IOCs\) associated with malware with the infosec community, AV vendors and threat intelligence providers.|[https://threatfox.abuse.ch/downloads/misp/manifest.json](https://threatfox.abuse.ch/downloads/misp/manifest.json)|

    **Note:**

    Only REST endpoint URLs ending with \[`/manifest.json`\] are supported for MISP feed types.

4.  Select **Edit** to edit the feed and make necessary updates.

5.  Select **Save** to apply the changes.


**Parent Topic:**[View Threat Intel Feeds](../concept/base-system-threat-intel-feeds.md)

