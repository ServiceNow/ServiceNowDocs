---
title: Sightings
description: Sightings denote that an indicator or object was seen. Objects may be a malware, tool, threat actor, and so on.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [IoC Repository, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Sightings

Sightings denote that an indicator or object was seen. Objects may be a malware, tool, threat actor, and so on.

Sightings track who and what is the target, how attacks are carried out, and to track trends in attack behavior.

The Sighting relationship object contains extra properties not present in the generic relationship objects. These extra properties represent data specific to sighting relationships.

For example, a count, or representing how many times something was seen.

Sighting is captured as a relationship because you cannot have a sighting unless you have something that has been sighted.

-   What was sighted, such as the malware, campaign, or other SDO
-   Who sighted it and/or where it was sighted, represented as an identity
-   What was seen on systems and networks, represented as observed data

-   **[Define indicator sightings](../task/define-indicator-sightings.md)**  
Define sightings that denote that an indicator was seen.
-   **[Define object sightings](../task/define-object-sightings.md)**  
Define object sighting that describes that an object \(malware, tool, threat actor, and so on\) was seen.

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

[Locations](threat-intelligence-locations.md)

[Malware](threat-intelligence-malware.md)

[Malware analysis](threat-intelligence-malware-analysis.md)

[Observed data](threat-intelligence-observed-data.md)

[Threat actors](threat-actors.md)

[Threat groupings](threat-groupings.md)

[Marking definitions](marking-definitions.md)

[Threat notes](threat-intelligence-threat-notes.md)

[Threat opinions](threat-opinions.md)

[Threat reports](threat-reports.md)

[Tools](tools.md)

[Vulnerabilities](vulnerabilities.md)

[Relationships](stix-relationships.md)

[STIX Visualizer](stix-visualizer.md)

