---
title: Relationships
description: Use the relationship objects to link together two SDOs or STIX Cyber-observable Objects \(SCOs\) to describe how they relate to each other.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/stix-relationships.html
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
</table>-   **[Define object-object relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/define-object-object.md)**  
Define relationships between SDOs, except the indicator object.
-   **[Define object-indicator relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/define-object-indicator.md)**  
Define relationships between the indicator object and other SDOs.
-   **[Define object-observable relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/define-object-observable.md)**  
Define relationships between SDOs and the observable object \(SCO\).

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

[Locations]()

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

[STIX Visualizer]()

