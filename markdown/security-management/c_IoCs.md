---
title: Indicators of compromise
description: Indicators of Compromise \(IoC\) are artifacts observed on a network or operating system that are likely to indicate an intrusion. Typical IoCs are virus signatures and IP addresses, MD5 hashes of malware files or URLs, or domain names. IoC applies for STIX 1.1 and 2.x.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [IoC Repository, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Indicators of compromise

Indicators of Compromise \(IoC\) are artifacts observed on a network or operating system that are likely to indicate an intrusion. Typical IoCs are virus signatures and IP addresses, MD5 hashes of malware files or URLs, or domain names. IoC applies for STIX 1.1 and 2.x.

An IoC can be a single observable or a collection of observables \(for example, a single known bad URL or the presence of a specific file and a couple of specific registry key values\).

After IoCs have been identified in a process of incident response and computer forensics, they can be used for early detection of future attack attempts using intrusion detection systems and antivirus software.

IoC applies for STIX 1.1 and 2.x.

-   **[View an IoC](../task/t_AddIoCs.md)**  
IoCs, sometimes referred to as indicators, are most typically retrieved from a threat data source as STIX data. If needed, you can also create IoCs.
-   **[Add a related observable to an IoC](../task/t_AddObservToIoC.md)**  
In addition to importing observables as STIX data, you can add related observables to an IoC manually.
-   **[Add a related attack mode/method to an IoC](../task/t_AddRelatedAttackModeToIoc.md)**  
In addition to importing related attack modes/methods as STIX data, you can add related attack modes/methods to an IoC manually.
-   **[Identify associated indicator types](../task/t_IdentifyAssociatedIndicatorTypes.md)**  
If an IoC has no associated indicator types defined, it tracks all types of observables. However, if you associate one or more types of indicators to an IoC, it limits the types of observables that can be associated with the IoC.
-   **[Identify indicator sources](../task/t_IdentifyIndicatorSources.md)**  
Indicator sources are normally tracked automatically as part of the threat import process, but more sources can be manually added.
-   **[Add associated tasks to an IoC](../task/t_AddAssociatedTasksToIoC.md)**  
In addition to importing associated tasks \(such as changes and incidents\) as STIX data, you can add them to an IoC manually.

**Parent Topic:**[IoC Repository](ioc-repository.md)

**Related topics**  


[Attack modes and methods](c_AttackModeMethod.md)

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

[Relationships](stix-relationships.md)

[STIX Visualizer](stix-visualizer.md)

