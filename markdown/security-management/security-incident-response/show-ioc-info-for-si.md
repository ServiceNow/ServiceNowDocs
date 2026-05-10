---
title: Show IoC information for a security incident
description: You can view IoC information, such as observables and sightings search results associated with a security incident.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Manage observables, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Show IoC information for a security incident

You can view IoC information, such as observables and sightings search results associated with a security incident.

## Before you begin

Role required: sn\_si.basic

## Procedure

1.  If it is not already open, open the security incident for which you want to view IoC-related information.

2.  Click the **Show IoC** related link.

3.  Click any of the related lists to view or add information for the security incident.

    |Tab|Description|
    |---|-----------|
    |Observables|View or manually add or edit observables associated with the security incident. For more information, see [Manage observables](../concept/sec-inc-observables.md).|
    |Associated Indicators|If Threat Intelligence is activated, you can view any other indicators associated with any of the same threat records.|
    |Sightings Search Results|Contains Sightings Search results.|
    |Sightings Search Details|Contains Sightings Search record details.|
    |Threat Lookups|Stores enrichment data from malware detection systems. This tab only appears when the Threat Intelligence plugin is installed.|
    |Associated Attack Modes/Methods|If Threat Intelligence is activated, you can view any other attack types associated with any of the same threat records.|
    |Security Scan Requests|If Threat Intelligence is activated, you can view scan and lookup requests attached to the security incident.|
    |Resources with Similar IoC|If Threat Intelligence is activated, you can view any other resources with similar indicators.|
    |Users with Similar IoC|If Threat Intelligence is activated, you can view any other users with similar indicators.|

4.  Click any of the following related links to further update the security incident:

    -   [Show Affected Items](show-affected-items-for-si.md)
    -   [Show Related Items](show-related-items-for-si.md)
    -   [Show Enrichment Data](show-enrich-data-for-si.md)
    -   [Show Response Tasks](show-response-tasks-for-si.md)
5.  When you have completed your entries, click **Submit**.


