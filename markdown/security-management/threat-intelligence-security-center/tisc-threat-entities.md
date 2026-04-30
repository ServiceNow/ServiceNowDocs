---
title: Threat Entities
description: The Threat Entities module provides structured records used to manage threat intelligence objects in the TISC. These records align with STIX domain object concepts and help standardize how threat activity is documented and analyzed.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-03-05"
reading_time_minutes: 4
breadcrumb: [TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Threat Entities

The Threat Entities module provides structured records used to manage threat intelligence objects in the TISC. These records align with STIX domain object concepts and help standardize how threat activity is documented and analyzed.

Use this module to create and manage entities such as:

-   **Attack Patterns** to document adversary tactics and techniques.
-   **Campaigns** to track coordinated threat activity over time.
-   **Courses of Action** to define recommended remediation steps.
-   **Identities** to represent individuals, groups, or organizations.
-   **Infrastructure** to record systems and services used in operations.
-   **Intrusion Sets** to group related threat activity.
-   **Malware** and **Malware Analysis** records for malicious tools and findings.
-   **Threat Actors** to represent adversaries.
-   **Threat Events**, **Threat Reports**, **Threat Notes**, and **Threat Opinion** to capture contextual intelligence.
-   **Marking Definitions** to apply data handling classifications.

-   **[Attack Patterns](tisc-attack-patterns.md)**  
Attack patterns are a type of Tactics, Techniques, and Procedures \(TTPs\) that describe the methods that adversaries attempt to compromise targets.
-   **[Campaign](campaign.md)**  
Campaign is defined as grouping of adversarial behaviors that describes a set of malicious activities or attacks, sometimes called waves that occur over a period of time against a specific set of targets.
-   **[Courses of Action](course-of-action.md)**  
Courses of action is an action taken either to prevent an attack or to respond to an attack that is in progress.
-   **[Identity](identity.md)**  
Identities represent actual individuals, organizations or groups, and classes of individuals, systems, or groups. Identities apply for STIX 2.x.
-   **[Infrastructure](infrastructure.md)**  
The Infrastructure SDO represents a type of Tactics, Techniques, and Procedures \(TTPs\). They describe any systems, software services, and any associated physical or virtual resources intended to support some purpose of an attack. Infrastructure applies for STIX 2.x.
-   **[Intrusion Set](intrusion-set.md)**  
An Intrusion Set is a grouped set of adversarial behaviors and resources with common properties. An Intrusion Set usually involves a single organization. Intrusion set applies for STIX 2.x.
-   **[Location](location.md)**  
A Location represents a geographic location. Locations are primarily used to give context to other SDOs. Locations apply for STIX 2.x.
-   **[Malware](malware.md)**  
Malware is a type of TTP that represents malicious code. It refers to a program that is covertly inserted into a system. Malware applies for STIX 2.x.
-   **[Malware Analysis](malware-analysis.md)**  
Malware Analysis captures the metadata and results of a malware. Malware analysis applies for STIX 2.x.
-   **[Marking Definition](marking-definition.md)**  
The marking-definition object represents a specific marking. Data markings typically represent handling or sharing requirements for data.
-   **[Object Sighting](object-sighting.md)**  
Sightings denote that an object was seen. Objects may be a malware, tool, threat actor, and so on.
-   **[Observed Data](tisc-observed-data.md)**  
Observed Data conveys information about cyber security-related entities such as files, systems, and networks using the STIX Cyber-observable Objects \(SCOs\). Observed data applies for STIX 2.x.
-   **[Threat Actor](threat-actor.md)**  
Threat Actors are individuals, groups, or organizations who act with malicious intent. Threat actors applies for STIX 2.x.
-   **[Threat Event](threat-event.md)**  
An event or situation that has the potential for causing undesirable consequences or impact.
-   **[Threat Grouping](threat-grouping.md)**  
A Threat Groupings object explicitly asserts that the referenced STIX Objects have a shared context. Threat groupings applies for STIX 2.x.
-   **[Threat Note](threat-note.md)**  
A Threat Note conveys informative text to provide additional analysis not contained in the STIX Objects, Marking Definition objects, or Language Content objects which the Note relates to. Threat notes applies for STIX 2.x.
-   **[Threat Opinion](threat-opinion.md)**  
An Opinion is an assessment of the accuracy of the information in a STIX Object produced by a different entity. Threat opinions apply for STIX 2.x.
-   **[Threat Report](threat-report.md)**  
Threat Reports are collections of threat intelligence focused on one or more topics. Threat reports apply for STIX 2.x.
-   **[Tool](tool.md)**  
Tools are legitimate software that are used by threat actors to perform attacks. Tools apply for STIX 2.x.

**Parent Topic:**[TISC Library Repository](tisc-ioc.md)

**Related topics**  


[Observables](observables.md)

[Indicators](indicator.md)

[Other Objects](tisc-other-objects.md)

[Vulnerability](vulnerability.md)

[Define RSS Feeds](../task/define-rss-feeds.md)

[Working with Reports in TISC](tisc-reports-lib-view.md)

[MITRE-ATT&amp;CK Repository](tisc-mitre-att-ck-framework-overview.md)

[Relationships Objects](relationship-objects.md)

[Potential Relationships](potential-relationships.md)

[Vulnerability relationship mapping](tisc-vul-relationship-map.md)

[Observables](observables.md)

[Indicators](indicator.md)

