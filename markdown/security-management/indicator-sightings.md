---
title: Sightings
description: Sightings denote that an indicator or object was seen. Objects may be a malware, tool, threat actor, and so on.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/indicator-sightings.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [IoC Repository, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Sightings

Sightings denote that an indicator or object was seen. Objects may be a malware, tool, threat actor, and so on.

Sightings track who and what is the target, how attacks are carried out, and to track trends in attack behavior.

The Sighting relationship object contains extra properties not present in the generic relationship objects. These extra properties represent data specific to sighting relationships.

For example, a count, or representing how many times something was seen.

Sighting is captured as a relationship because you cannot have a sighting unless you have something that has been sighted.

-   What was sighted, such as the malware, campaign, or other SDO
-   Who sighted it and/or where it was sighted, represented as an identity
-   What was seen on systems and networks, represented as observed data

-   **[Define indicator sightings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/define-indicator-sightings.md)**  
Define sightings that denote that an indicator was seen.
-   **[Define object sightings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/define-object-sightings.md)**  
Define object sighting that describes that an object \(malware, tool, threat actor, and so on\) was seen.

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

[Tools]()

[Vulnerabilities]()

[Relationships]()

[STIX Visualizer]()

