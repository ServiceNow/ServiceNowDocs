---
title: Relationships Objects
description: Use the relationships objects to link together two observables or an observable and SDO to explain how they relate to each other.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Relationships Objects

Use the relationships objects to link together two observables or an observable and SDO to explain how they relate to each other.

STIX Relationship Objects \(SROs\) represent types of relationships between various STIX objects. The following relationship objects are available:

-   **Observable-Observable Relationship**: This object defines relationships between observables.
-   **Object-Object Relationship**: This object defines relationships between SDOs, except the indicator object. An example of an object-object defined relationship is that an attack pattern delivers a malware.
-   **Object-Observable Relationship**: This object defines relationships between SDOs and the observable object \(SCO\). An example of an object-observable defined relationship is that an infrastructure consists of cyber observable objects which provides information of a potential attack.
-   **Object-indicator Relationship**: This object defines relationships between SDOs and the indicator object.
-   **Indicator-Indicator Relationships**: This object defines relationships between indicator objects.
-   **Indicator-Observable Relationship**: This object defines relationships between the indicator object and other SDOs. An example of an object-indicator defined relationship is that an indicator detects evidence of a campaign.

<table id="table_ihr_xkv_xmb"><thead><tr><th>

Relationship Object

</th><th>

Example Source

</th><th>

Example Target

</th><th>

Example Description

</th></tr></thead><tbody><tr><td>

Observable-Observable Relationships

</td><td>

IP address, domain name

</td><td>

 

</td><td>

This relationship describes between the observables.

</td></tr><tr><td>

Object-Object Relationships

</td><td>

Attack-pattern

</td><td>

Malware

</td><td>

This relationship describes that this Attack Pattern is used to deliver this malware instance \(or family\).

</td></tr><tr><td>

Object-Observable Relationships

</td><td>

 

</td><td>

 

</td><td>

This relationship describes between the objects and observables.

</td></tr><tr><td>

Object-Indicator Relationships

</td><td>

Indicator

</td><td>

Attack-Pattern, Campaign, Infrastructure, Intrusion-set, Malware, Threat-actor, Tool

</td><td>

This relationship describes that the indicator can detect evidence of the related attack pattern, campaign, infrastructure, intrusion set, malware, threat actor, or tool.The evidence may not be direct. For example, the indicator may detect secondary evidence of the campaign such as malware that is commonly used by that particular campaign.

</td></tr><tr><td>

Indicator -Indicator Relationships

</td><td>

Infrastructure

</td><td>

Observed data

</td><td>

This relationship describes that the indicator is created based on information from an observed data object.An example of an object-observable defined relationship is that an infrastructure consists of cyber observable objects which provides information of a potential attack.

</td></tr><tr><td>

Indicator-Observable

</td><td>

 

</td><td>

 

</td><td>

This relationship describes between the indicators and observables.

</td></tr></tbody>
</table>-   **[Define observable-observable relationships](../task/define-observable-observable.md)**  
Define relationships between observables.
-   **[Define object-object relationships](../task/define-object-object-relationships.md)**  
Define relationships between SDOs, except the indicator object.
-   **[Define object-observable relationships](../task/define-object-observable-relationships.md)**  
Define relationships between SDOs and the observable object \(SCO\).
-   **[Define object-indicator relationships](../task/define-object-indicator-relationships.md)**  
Define relationships between the indicator object and other SDOs.
-   **[Define indicator-indicator relationships](../task/define-indicator-indicator-relationships.md)**  
Define relationships between the indicator object and other Use the relationships objects to link together two observables or an observable and SDO to explain how they relate to each other..
-   **[Define indicator-observable relationships](../task/define-indicator-observable-relationships.md)**  
Define relationships between the indicator object and other SDOs.

**Parent Topic:**[TISC Library Repository](tisc-ioc.md)

**Related topics**  


[Observables](observables.md)

[Indicators](indicator.md)

[Threat Entities](tisc-threat-entities.md)

[Other Objects](tisc-other-objects.md)

[Vulnerability Artifacts](vulnerability.md)

[View RSS Feeds](../task/define-rss-feeds.md)

[Working with Reports in TISC](tisc-reports-lib-view.md)

[MITRE-ATT&amp;CK Repository](tisc-mitre-att-ck-framework-overview.md)

[Potential Relationships](potential-relationships.md)

[Vulnerability relationship mapping](tisc-vul-relationship-map.md)

