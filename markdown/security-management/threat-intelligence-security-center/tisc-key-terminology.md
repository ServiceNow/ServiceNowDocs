---
title: TISC Key terminology
description: The terms defined below are used throughout the Threat Intelligence Security Center \(TISC\).
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Explore, Threat Intelligence Security Center, Security Operations]
---

# TISC Key terminology

The terms defined below are used throughout the Threat Intelligence Security Center \(TISC\).

<table id="table_rvc_3t1_pzb"><thead><tr><th>

Terminology

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Data Processing

</td><td>

A Threat Intelligence Platform \(TIP\) is a technology solution that collects, aggregates, and organizes threat intelligence data from various sources and patterns. Threat intelligence is the data that is collected, processed, and analyzed to understand a threat actors targets and attack behaviors.

</td></tr><tr><td>

Observables

</td><td>

Observables represent stateful properties \(such as the MD5 hash of a file or the value of a registry key\) or measurable events \(such as the creation of a registry key or the deletion of a file\) that are pertinent to the operation of computers and networks. For more information, see [Observables](observables.md).

</td></tr><tr><td>

Indicators

</td><td>

Indicators contain a pattern that can be used to detect suspicious or malicious cyber activity. For example, an Indicator may be used to represent a set of malicious domains and use the STIX Patterning Language to specify these domains.The Indicator SDO contains a simple textual description, the Kill Chain Phases that it detects behavior in, a time window for when the Indicator is valid or useful, and a required **pattern** property to capture a structured detection pattern. For more information, see [Indicators](indicator.md).

</td></tr><tr><td>

Objects

</td><td>

Defines the set of STIX Domain Objects \(SDOs\), each of which corresponds to a unique concept commonly represented in Cyber Threat Intelligence \(CTI\).Using SDOs and STIX Relationship Objects \(SROs\) as building blocks, individuals can create and share broad and comprehensive cyber threat intelligence. For more information, see [TISC Library Repository](tisc-ioc.md).

</td></tr><tr><td>

Relationships

</td><td>

A relationship is a link between two observables or two SDOs or Observable and SDO that describes the way in which the objects are related.Relationships can be represented using an external STIX Relationship Object \(SRO\) or, in some cases, through certain properties which store an identifier reference that comprises an embedded relationship. For more information, see [Relationships Objects](relationship-objects.md).

</td></tr></tbody>
</table>**Parent Topic:**[Explore](../reference/threat-intelligence-security-center-overview.md)

**Related topics**  


[Home page in TISC Workspace](../task/view-threat-intelligence-security-center-homepage.md)

