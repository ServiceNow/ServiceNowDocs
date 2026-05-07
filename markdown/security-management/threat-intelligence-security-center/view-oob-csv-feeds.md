---
title: View CSV Feeds
description: View configured CSV feeds to monitor data import sources and their current status. Use this to verify feed configurations and troubleshoot import issues.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-04-28"
reading_time_minutes: 1
breadcrumb: [View Threat Intel Feeds, Threat Intelligence Feeds, Integrate, Threat Intelligence Security Center, Security Operations]
---

# View CSV Feeds

View configured CSV feeds to monitor data import sources and their current status. Use this to verify feed configurations and troubleshoot import issues.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Select the **Integrations** icon.

3.  Select **CSV**.

    The CSV feeds within the base system are explained in the following table.

    |ThreatFeed|Description|URL|
    |----------|-----------|---|
    |PhishStats|Phishing URLs from the past 30 days from PhishStats.|[https://phishstats.info/phish\_score.csv](https://phishstats.info/phish_score.csv)|
    |Abuse.ch SSL Certificate Denylist|The SSL Certificate Denylist \(CSV\) is a CSV that contains SHA1 Fingerprint of all SSL certificates denied on SSLBL.|[https://sslbl.abuse.ch/blacklist/sslblacklist.csv](https://sslbl.abuse.ch/blacklist/sslblacklist.csv)|
    |Botnet C2 IP Denylist|An SSL certificate can be associated with one or more servers \(IP address:port combination\). SSLBL collects IP addresses that are running with an SSL certificate denied on SSLBL. These are usually botnet Command&amp;Control servers \(C&amp;C\). SSLBL publishes a denylist containing these IPs to detect botnet C2 traffic from infected machines.|[https://sslbl.abuse.ch/blacklist/sslipblacklist.csv](https://sslbl.abuse.ch/blacklist/sslipblacklist.csv)|
    |Phishtank online|NA|[https://data.phishtank.com/data/online-valid.csv](https://data.phishtank.com/data/online-valid.csv)|

4.  Select **Edit** to edit the feed and make necessary updates.

5.  Select **Save** to apply the changes.


**Parent Topic:**[View Threat Intel Feeds](../concept/base-system-threat-intel-feeds.md)

