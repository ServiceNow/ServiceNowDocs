---
title: Locations
description: A Location represents a geographic location. Locations are primarily used to give context to other SDOs. Locations apply for STIX 2.x.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-locations.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [IoC Repository, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Locations

A Location represents a geographic location. Locations are primarily used to give context to other SDOs. Locations apply for STIX 2.x.

The location may contain, some or all of the following: region \(North America\), civic address \(New York, US\), latitude, and longitude.

The Location SDO may relate to an Identity or Intrusion Set to indicate that the identity or intrusion set is in that location. It can also relate to a malware or attack pattern to indicate that the target victim is in a particular location.

For example, a Location could be used in a relationship to describe that the Bourgeois Swallow intrusion set originates from Eastern Europe.

At least one of the following properties or sets of properties must be provided:

-   region
-   country
-   latitude and longitude

-   **[Define Location](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/define-location.md)**  
Define a geographic location to provide more context to other SDOs.

**Parent Topic:**[IoC Repository](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/ioc-repository.md)

**Related topics**  


[Attack modes and methods]()

[Indicators of compromise]()

[Observables]()

[Attack patterns]()

[Campaigns]()

[Course of actions]()

[Identities]()

[Infrastructure]()

[Intrusion set]()

[Malware]()

[Malware analysis]()

[Observed data]()

[Threat actors]()

[Threat groupings]()

[Marking definitions]()

[Threat notes]()

[Threat opinions]()

[Threat reports]()

[Sightings]()

[Tools]()

[Vulnerabilities]()

[Relationships]()

[STIX Visualizer]()

