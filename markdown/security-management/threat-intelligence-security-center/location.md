---
title: Location
description: A Location represents a geographic location. Locations are primarily used to give context to other SDOs. Locations apply for STIX 2.x.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Threat Entities, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Location

A Location represents a geographic location. Locations are primarily used to give context to other SDOs. Locations apply for STIX 2.x.

The location may contain, some or all of the following: region \(North America\), civic address \(New York, US\), latitude, and longitude.

The Location SDO may relate to an Identity or Intrusion Set to indicate that the identity or intrusion set is in that location. It can also relate to a malware or attack pattern to indicate that the target victim is in a particular location.

For example, a Location could be used in a relationship to describe that the Bourgeois Swallow intrusion set originates from Eastern Europe.

At least one of the following properties or sets of properties must be provided:

-   region
-   country
-   latitude and longitude

-   **[Define Location](../task/tisc-define-location.md)**  
Define a geographic location to provide more context to other TISC entities.

**Parent Topic:**[Threat Entities](tisc-threat-entities.md)

