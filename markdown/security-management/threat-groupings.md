---
title: Threat groupings
description: A Threat Groupings object explicitly asserts that the referenced STIX Objects have a shared context. Threat groupings applies for STIX 2.x.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-groupings.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [IoC Repository, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Threat groupings

A Threat Groupings object explicitly asserts that the referenced STIX Objects have a shared context. Threat groupings applies for STIX 2.x.

A Threat Groupings object represents a set of data that, given sufficient analysis, matures to convey an incident or threat report as a STIX Report object. For example, a Grouping could be used to characterize an ongoing investigation into a security event or incident.

A Threat Groupings object could also be used to assert that the referenced STIX Objects are related to an ongoing analysis process. For example, a threat analyst may collaborate with others in their trust community to examine a series of Campaigns and Indicators.

The Threat Grouping SDO contains a list of references to SDOs, SCOs, and SROs, along with an explicit statement of the context shared by the content, a textual description, and the name of the grouping.

-   **[Define threat groupings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/define-threat-groupings.md)**  
Define threat groupings as objects that have a shared context.

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

[Marking definitions]()

[Threat notes]()

[Threat opinions]()

[Threat reports]()

[Sightings]()

[Tools]()

[Vulnerabilities]()

[Relationships]()

[STIX Visualizer]()

