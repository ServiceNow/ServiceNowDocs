---
title: System Properties for CrowdStrike
description: The following details the system properties for CrowdStrike.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure custom CrowdStrike feed, View Custom Feed, View Threat Intel Feeds, Threat Intelligence Feeds, Integrate Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# System Properties for CrowdStrike

The following details the system properties for CrowdStrike.

1.  sn\_sec\_tisc.crowdstrike\_actor\_batch\_size: Denotes the number of actors to be pulled in a single API call. Note: applicable only when the integration doesn't find the necessary present in the system.
    -   Type: Integer
    -   Value: 250
2.  sn\_sec\_tisc.crowdstrike\_api\_limit: Number of records to fetch at a time from CrowdStrike. Higher the number, more the memory would consumed for processing the payload.
    -   Type: Integer
    -   Value: 1000
3.  sn\_sec\_tisc.crowdstrike\_indicator\_batch\_size: Denotes the number of indicators to be pulled in a single API call. Note: applicable only when the integration doesn't find the necessary present in the system.
    -   Type: Integer
    -   Value: 150
4.  sn\_sec\_tisc.crowdstrike\_offset\_limit\_total: The allowed total of offset and limit from CrowdStrike API.
    -   Type: Integer
    -   Value: 50000
5.  sn\_sec\_tisc.crowdstrike\_report\_batch\_size: Denotes the number of reports to be pulled in a single API call. Note: applicable only when the integration doesn't find the necessary present in the system.
    -   Type: Integer
    -   Value: 50

**Parent Topic:**[Configure custom CrowdStrike feed](../task/premium-threat-feed-for-crowdstrike.md)

