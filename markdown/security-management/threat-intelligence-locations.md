---
title: Locations
description: A Location represents a geographic location. Locations are primarily used to give context to other SDOs. Locations apply for STIX 2.x.
locale: en-US
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

-   **[Define Location](../task/define-location.md)**  
Define a geographic location to provide more context to other SDOs.

**Parent Topic:**[IoC Repository](ioc-repository.md)

**Related topics**  


[Attack modes and methods](c_AttackModeMethod.md)

[Indicators of compromise](c_IoCs.md)

[Observables](c_Observables.md)

[Attack patterns](attack-patterns.md)

[Campaigns](threat-intelligence-campaigns.md)

[Course of actions](threat-intelligence-course-actions.md)

[Identities](threat-intelligence-identities.md)

[Infrastructure](threat-intelligence-infrastructure.md)

[Intrusion set](threat-intelligence-intrusion-sets.md)

[Malware](threat-intelligence-malware.md)

[Malware analysis](threat-intelligence-malware-analysis.md)

[Observed data](threat-intelligence-observed-data.md)

[Threat actors](threat-actors.md)

[Threat groupings](threat-groupings.md)

[Marking definitions](marking-definitions.md)

[Threat notes](threat-intelligence-threat-notes.md)

[Threat opinions](threat-opinions.md)

[Threat reports](threat-reports.md)

[Sightings](indicator-sightings.md)

[Tools](tools.md)

[Vulnerabilities](vulnerabilities.md)

[Relationships](stix-relationships.md)

[STIX Visualizer](stix-visualizer.md)

