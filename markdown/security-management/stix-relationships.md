---
title: Relationships
description: Use the relationship objects to link together two SDOs or STIX Cyber-observable Objects \(SCOs\) to describe how they relate to each other.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [IoC Repository, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Relationships

Use the relationship objects to link together two SDOs or STIX Cyber-observable Objects \(SCOs\) to describe how they relate to each other.

STIX Relationship Objects \(SROs\) represent types of relationships between various STIX objects. The following relationship objects are available:

-   **Object-Object Relationship**: This object defines relationships between SDOs, except the indicator object. An example of an object-object defined relationship is that an attack pattern delivers a malware.
-   **Object-Indicator Relationship**: This object defines relationships between the indicator object and other SDOs. An example of an object-indicator defined relationship is that an indicator detects evidence of a campaign.
-   **Object-Observable Relationship**: This object defines relationships between SDOs and the observable object \(SCO\). An example of an object-observable defined relationship is that an infrastructure consists of cyber observable objects which provides information of a potential attack.

<table id="table_ihr_xkv_xmb"><thead><tr><th>

Relationship Object

</th><th>

Example Source

</th><th>

Example Target

</th><th>

Example Description

</th></tr></thead><tbody><tr><td>

Object-Object Relationships

</td><td>

Attack-pattern

</td><td>

Malware

</td><td>

This relationship describes that this Attack Pattern is used to deliver this malware instance \(or family\).

</td></tr><tr><td>

Object-Indicator Relationships

</td><td>

Indicator

</td><td>

Attack-Pattern, Campaign, Infrastructure, Intrusion-set, Malware, Threat-actor, Tool

</td><td>

This relationship describes that the indicator can detect evidence of the related attack pattern, campaign, infrastructure, intrusion set, malware, threat actor, or tool.The evidence may not be direct. For example, the indicator may detect secondary evidence of the campaign such as malware that is commonly used by that particular campaign.

</td></tr><tr><td>

Object-Observable Relationships

</td><td>

Infrastructure

</td><td>

Observed data

</td><td>

This relationship describes that the indicator is created based on information from an observed data object.An example of an object-observable defined relationship is that an infrastructure consists of cyber observable objects which provides information of a potential attack.

</td></tr></tbody>
</table>-   **[Define object-object relationships](../task/define-object-object.md)**  
Define relationships between SDOs, except the indicator object.
-   **[Define object-indicator relationships](../task/define-object-indicator.md)**  
Define relationships between the indicator object and other SDOs.
-   **[Define object-observable relationships](../task/define-object-observable.md)**  
Define relationships between SDOs and the observable object \(SCO\).

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

[Sightings](indicator-sightings.md)

[Tools](tools.md)

[Vulnerabilities](vulnerabilities.md)

[STIX Visualizer](stix-visualizer.md)

