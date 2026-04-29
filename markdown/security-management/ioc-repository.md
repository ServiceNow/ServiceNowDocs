---
title: IoC Repository
description: IoC repository contains STIX objects, each of these objects contain a specific piece of information.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# IoC Repository

IoC repository contains STIX objects, each of these objects contain a specific piece of information.

When you combine STIX objects together through relationships, you allow for easy or complex representations of Cyber Threat Intelligence \(CTI\).

Threat Intelligence supports STIX versions 1.1, 2.0, and 2.1.

-   **[Attack modes and methods](c_AttackModeMethod.md)**  
Attack modes and methods, sometimes referred to as Tactics, Techniques, and Procedures \(TTPs\), are representations of how cyber adversaries behave. They characterize what these adversaries do and how they do it, in increasing levels of detail. Attack modes and methods apply for STIX 1.1.
-   **[Indicators of compromise](c_IoCs.md)**  
Indicators of Compromise \(IoC\) are artifacts observed on a network or operating system that are likely to indicate an intrusion. Typical IoCs are virus signatures and IP addresses, MD5 hashes of malware files or URLs, or domain names. IoC applies for STIX 1.1 and 2.x.
-   **[Observables](c_Observables.md)**  
Observables represent stateful properties \(such as the MD5 hash of a file or the value of a registry key\) or measurable events \(such as the creation of a registry key or the deletion of a file\) that are pertinent to the operation of computers and networks. Observables apply for STIX 1.1 and 2.x.
-   **[Attack patterns](attack-patterns.md)**  
Attack patterns are a type of Tactics, Techniques, and Procedures \(TTPs\) that describe the methods that adversaries attempt to compromise targets. Attack Patterns apply for STIX 2.x.
-   **[Campaigns](threat-intelligence-campaigns.md)**  
A Campaign is a grouping of adversarial behaviors. These behaviors describe a set of malicious activities or attacks that occur over time against a specific set of targets. Campaigns apply for STIX 2.x.
-   **[Course of actions](threat-intelligence-course-actions.md)**  
A course of action is an action taken either to prevent an attack or to respond to an attack that is in progress. Course of actions apply for STIX 2.x.
-   **[Identities](threat-intelligence-identities.md)**  
Identities represent actual individuals, organizations, or groups \(ACME, Inc.\) and classes of individuals, systems, or groups \(the finance sector\). Identities apply for STIX 2.x.
-   **[Infrastructure](threat-intelligence-infrastructure.md)**  
The Infrastructure SDO represents a type of Tactics, Techniques, and Procedures \(TTPs\). They describe any systems, software services, and any associated physical or virtual resources intended to support some purpose of an attack. Infrastructure applies for STIX 2.x.
-   **[Intrusion set](threat-intelligence-intrusion-sets.md)**  
An Intrusion Set is a grouped set of adversarial behaviors and resources with common properties. An Intrusion Set usually involves a single organization. Intrusion set applies for STIX 2.x.
-   **[Locations](threat-intelligence-locations.md)**  
A Location represents a geographic location. Locations are primarily used to give context to other SDOs. Locations apply for STIX 2.x.
-   **[Malware](threat-intelligence-malware.md)**  
Malware is a type of TTP that represents malicious code. It refers to a program that is covertly inserted into a system. Malware applies for STIX 2.x.
-   **[Malware analysis](threat-intelligence-malware-analysis.md)**  
Malware Analysis captures the metadata and results of a malware. Malware analysis applies for STIX 2.x.
-   **[Observed data](threat-intelligence-observed-data.md)**  
Observed Data conveys information about cyber security-related entities such as files, systems, and networks using the STIX Cyber-observable Objects \(SCOs\). Observed data applies for STIX 2.x.
-   **[Threat actors](threat-actors.md)**  
Threat Actors are individuals, groups, or organizations who act with malicious intent. Threat actors applies for STIX 2.x.
-   **[Threat groupings](threat-groupings.md)**  
A Threat Groupings object explicitly asserts that the referenced STIX Objects have a shared context. Threat groupings applies for STIX 2.x.
-   **[Marking definitions](marking-definitions.md)**  
The marking definitions object represents a specific marking.
-   **[Threat notes](threat-intelligence-threat-notes.md)**  
A Threat Note conveys informative text to provide additional analysis not contained in the STIX Objects, Marking Definition objects, or Language Content objects which the Note relates to. Threat notes applies for STIX 2.x.
-   **[Threat opinions](threat-opinions.md)**  
An Opinion is an assessment of the accuracy of the information in a STIX Object produced by a different entity. Threat opinions apply for STIX 2.x.
-   **[Threat reports](threat-reports.md)**  
Threat Reports are collections of threat intelligence focused on one or more topics. Threat reports apply for STIX 2.x.
-   **[Sightings](indicator-sightings.md)**  
Sightings denote that an indicator or object was seen. Objects may be a malware, tool, threat actor, and so on.
-   **[Tools](tools.md)**  
Tools are legitimate software that are used by threat actors to perform attacks. Tools apply for STIX 2.x.
-   **[Vulnerabilities](vulnerabilities.md)**  
A Vulnerability is a weakness or defect in a software or hardware component that attackers exploit. Vulnerabilities apply for STIX 2.x.
-   **[Relationships](stix-relationships.md)**  
Use the relationship objects to link together two SDOs or STIX Cyber-observable Objects \(SCOs\) to describe how they relate to each other.
-   **[STIX Visualizer](stix-visualizer.md)**  
The STIX Visualizer visually represents the structure of the STIX object and its relationship.

**Parent Topic:**[Threat Intelligence](../reference/threat-intel-landing-page.md)

**Related topics**  


[Understanding Threat Intelligence](understanding-threat-intel.md)

[Set up Threat Intelligence](c_GetStartedWithThreatIntel.md#)

[MITRE-ATT&amp;CK framework overview](about-mitre-attack.md)

[MITRE D3FEND framework](mitre-d3fend-framework.md)

[Threat Intelligence administration](../reference/r_ThreatRespAdmin.md)

[Threat Intelligence integrations](threat-intelligence-integrations.md)

[Threat Intelligence Orchestration](../../threat-intelligence-orchestration/concept/c_ThreatIntelligenceOrchestration.md)

[Security Case Management](../../threat-intelligence-case-management/concept/case-mgmt.md)

