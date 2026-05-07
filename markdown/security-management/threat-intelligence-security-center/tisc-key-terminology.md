---
title: TISC Key terminology
description: Key terms and definitions used in TISC to help you understand threat intelligence concepts and navigate the interface effectively.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Explore, Threat Intelligence Security Center, Security Operations]
---

# TISC Key terminology

Key terms and definitions used in TISC to help you understand threat intelligence concepts and navigate the interface effectively.

<table id="table_rvc_3t1_pzb"><thead><tr><th>

Terminology

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Data Processing

</td><td>

A Threat Intelligence Platform \(TIP\) collects, aggregates, and organizes threat intelligence data from various sources and patterns. Threat intelligence is data that is collected, processed, and analyzed to understand threat actor targets and attack behaviors.

</td></tr><tr><td>

Observables

</td><td>

Observables represent stateful properties or measurable events pertinent to computer and network operations. Examples include MD5 file hashes, registry key values, registry key creation, or file deletion. For more information, see [Observables](../concept/observables.md).

</td></tr><tr><td>

Indicators

</td><td>

Indicators contain patterns used to detect suspicious or malicious cyber activity. For example, an Indicator can represent malicious domains using the STIX Patterning Language.The Indicator SDO contains a textual description, Kill Chain Phases for detected behavior, a validity time window, and a required **pattern** property for structured detection patterns. For more information, see [Indicators](../concept/indicator.md).

</td></tr><tr><td>

Objects

</td><td>

Defines STIX Domain Objects \(SDOs\), each corresponding to a unique concept in cyberthreat Intelligence \(CTI\).Using SDOs and STIX Relationship Objects \(SROs\), you can create and share comprehensive cyberthreat intelligence. For more information, see [TISC Library Repository](../concept/tisc-ioc.md).

</td></tr><tr><td>

Relationships

</td><td>

A relationship links two observables, two SDOs, or an Observable and SDO, describing how the objects relate.Relationships can be represented using an external STIX Relationship Object \(SRO\) or through properties that store identifier references for embedded relationships. For more information, see [Relationships Objects](../concept/relationship-objects.md).

</td></tr></tbody>
</table>**Parent Topic:**[Explore](threat-intelligence-security-center-overview.md)

**Related topics**  


[TISC Workspace](../task/view-threat-intelligence-security-center-homepage.md)

[TISC Workspace](../task/view-threat-intelligence-security-center-homepage.md)

