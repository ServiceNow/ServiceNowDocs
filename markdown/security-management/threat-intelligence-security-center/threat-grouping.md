---
title: Threat Grouping
description: A Threat Groupings object explicitly asserts that the referenced STIX Objects have a shared context. Threat groupings applies for STIX 2.x.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Threat Entities, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Threat Grouping

A Threat Groupings object explicitly asserts that the referenced STIX Objects have a shared context. Threat groupings applies for STIX 2.x.

A Threat Groupings object represents a set of data that, given sufficient analysis, matures to convey an incident or threat report as a STIX Report object. For example, a Grouping could be used to characterize an ongoing investigation into a security event or incident.

A Threat Groupings object could also be used to assert that the referenced STIX Objects are related to an ongoing analysis process. For example, a threat analyst may collaborate with others in their trust community to examine a series of Campaigns and Indicators.

The Threat Grouping SDO contains a list of references to SDOs, SCOs, and SROs, along with an explicit statement of the context shared by the content, a textual description, and the name of the grouping.

-   **[Define Threat Grouping](../task/define-threat-grouping.md)**  
Define threat groupings as objects that have a shared context.

**Parent Topic:**[Threat Entities](tisc-threat-entities.md)

