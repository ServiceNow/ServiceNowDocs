---
title: View STIX HTTPs Feeds
description: View and manage STIX threat intelligence feeds that provide security data to your ServiceNow instance. Use this to monitor feed status and troubleshoot connection issues.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [View Threat Intel Feeds, Threat Intelligence Feeds, Integrate, Threat Intelligence Security Center, Security Operations]
---

# View STIX HTTPs Feeds

View and manage STIX threat intelligence feeds that provide security data to your ServiceNow instance. Use this to monitor feed status and troubleshoot connection issues.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Select **Integrations** icon.

3.  Select **STIX HTTPs**.

    The following table describes the STIX HTTPs feeds within the base system.

    |ThreatFeed|Description|URL|
    |----------|-----------|---|
    |MITRE - Mobile ATT&amp;CK|This data collection holds STIX objects from Mobile ATT&amp;CK.|[https://raw.githubusercontent.com/mitre/cti/master/mobile-attack/mobile-attack.json](https://raw.githubusercontent.com/mitre/cti/master/mobile-attack/mobile-attack.json)|
    |MITRE - ICS ATT&amp;CK|This data collection holds STIX objects from ICS ATT&amp;CK.|[https://raw.githubusercontent.com/mitre/cti/master/ics-attack/ics-attack.json](https://raw.githubusercontent.com/mitre/cti/master/ics-attack/ics-attack.json)|
    |MITRE - Enterprise ATT&amp;CK|This data collection holds STIX objects from Enterprise ATT&amp;CK.|[https://raw.githubusercontent.com/mitre/cti/master/enterprise-attack/enterprise-attack.json](https://raw.githubusercontent.com/mitre/cti/master/enterprise-attack/enterprise-attack.json)|

4.  Select **Edit** to edit the feed and make necessary updates.

5.  Select **Save** to apply the changes.


**Parent Topic:**[View Threat Intel Feeds](../concept/base-system-threat-intel-feeds.md)

