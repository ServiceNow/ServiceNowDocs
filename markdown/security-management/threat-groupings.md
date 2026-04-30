---
title: Threat groupings
description: A Threat Groupings object explicitly asserts that the referenced STIX Objects have a shared context. Threat groupings applies for STIX 2.x.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [IoC Repository, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Threat groupings

A Threat Groupings object explicitly asserts that the referenced STIX Objects have a shared context. Threat groupings applies for STIX 2.x.

A Threat Groupings object represents a set of data that, given sufficient analysis, matures to convey an incident or threat report as a STIX Report object. For example, a Grouping could be used to characterize an ongoing investigation into a security event or incident.

A Threat Groupings object could also be used to assert that the referenced STIX Objects are related to an ongoing analysis process. For example, a threat analyst may collaborate with others in their trust community to examine a series of Campaigns and Indicators.

The Threat Grouping SDO contains a list of references to SDOs, SCOs, and SROs, along with an explicit statement of the context shared by the content, a textual description, and the name of the grouping.

-   **[Define threat groupings](../task/define-threat-groupings.md)**  
Define threat groupings as objects that have a shared context.

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

[Marking definitions](marking-definitions.md)

[Threat notes](threat-intelligence-threat-notes.md)

[Threat opinions](threat-opinions.md)

[Threat reports](threat-reports.md)

[Sightings](indicator-sightings.md)

[Tools](tools.md)

[Vulnerabilities](vulnerabilities.md)

[Relationships](stix-relationships.md)

[STIX Visualizer](stix-visualizer.md)

