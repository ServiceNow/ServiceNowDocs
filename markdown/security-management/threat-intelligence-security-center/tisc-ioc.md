---
title: TISC Library Repository
description: IoC repository contains STIX objects, each of these objects contain a specific piece of information.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# TISC Library Repository

IoC repository contains STIX objects, each of these objects contain a specific piece of information.

-   **[Observables](observables.md)**  
Observables represent stateful properties \(such as the MD5 hash of a file or the value of a registry key\) or measurable events \(such as the creation of a registry key or the deletion of a file\) that are pertinent to the operation of computers and networks.
-   **[Indicators](indicator.md)**  
Indicators are artifacts observed on a network or operating system that are likely to indicate an intrusion. Typical IoCs are virus signatures and IP addresses, MD5 hashes of malware files or URLs, or domain names.
-   **[Threat Entities](tisc-threat-entities.md)**  
The Threat Entities module provides structured records used to manage threat intelligence objects in the TISC. These records align with STIX domain object concepts and help standardize how threat activity is documented and analyzed.
-   **[Other Objects](tisc-other-objects.md)**  
Define and manage data classifications within TISC.
-   **[Vulnerability](vulnerability.md)**  
A Vulnerability is a weakness or defect in a software or hardware component that attackers exploit. Vulnerabilities apply for STIX 2.x.
-   **[Define RSS Feeds](../task/define-rss-feeds.md)**  
A threat intelligence feed is a real time, continuous data stream that gathers information related to cyber risks or threats. RSS Feeds provides an easy way to stay up to date with your favorite websites, such as blogs or latest cyber security news.
-   **[Working with Reports in TISC](tisc-reports-lib-view.md)**  
The Reports module in the Threat Intelligence Library section enables you to create, manage, and publish reports that use any intelligence available in the Threat Intelligence Library.
-   **[MITRE-ATT&amp;CK Repository](tisc-mitre-att-ck-framework-overview.md)**  
The MITRE-ATT&amp;CK repository is available under the Intelligence Library where the data from the MITRE sources are ingested.
-   **[Relationships Objects](relationship-objects.md)**  
Use the relationships objects to link together two observables or an observable and SDO to explain how they relate to each other.
-   **[Potential Relationships](potential-relationships.md)**  
The application uses automated correlation to establish potentially possible relationships between two SDOs, two Observables or an observable and SDO.
-   **[Vulnerability relationship mapping](tisc-vul-relationship-map.md)**  
Use many-to-many \(M2M\) relationship records to map connections between vulnerabilities and other entities.

**Parent Topic:**[Threat Intelligence Security Center Library](threat-intelligence-security-center-library.md)

**Related topics**  


[Understanding the Data Model](../reference/understanding-the-data-model.md)

[TISC Library Objects form view](tisc-library-home-page-view.md)

[Access Vulnerability Downstream actions](downstream-actions-from-the-vulnerability-form-view.md)

[Deleting threat intelligence library records](../task/tisc-delete-lib-records.md)

[Export intelligence data](../task/tisc-export-observables.md)

[Confirm Potential Relationships from Related Records](../task/confirm-potential-relationships.md)

[Automated Correlation](automated-correlation-rules.md)

