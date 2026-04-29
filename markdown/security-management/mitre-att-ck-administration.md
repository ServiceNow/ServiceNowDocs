---
title: MITRE-ATT&amp;CK administration
description: You can set up, map data sources, map overall technique detection coverage, and maintain the MITRE-ATT&amp;CK repository in the ServiceNow AI Platform.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# MITRE-ATT&amp;CK administration

You can set up, map data sources, map overall technique detection coverage, and maintain the MITRE-ATT&amp;CK repository in the ServiceNow AI Platform.

-   **[Get started with MITRE-ATT&amp;CK framework](../reference/get-started-with-mitre.md)**  
Review the following information before you start setting up your MITRE-ATT&amp;CK framework.
-   **[Understand the MITRE to STIX data model](../reference/understand-the-mitre-to-stix-data-model-mapping.md)**  
Review the terminology used by MITRE and STIX to efficiently use and understand the MITRE-ATT&amp;CK™ framework in the ServiceNow AI Platform.
-   **[Domain separation and MITRE-ATT&amp;CK](../reference/domain-separation-and-mitre-att-ck.md)**  
This domain separation overview pertains to MITRE-ATT&amp;CK. Domain separation allows you to separate data, processes, and administrative tasks into logical groupings called domains. You can then control several aspects of this separation, including which users can see and access data.
-   **[Set up the MITRE-ATT&amp;CK framework](../task/setup-mitre-profile.md)**  
Activate the MITRE-ATT&amp;CK profile, and set up a scheduled job so that you can set up MITRE-ATT&amp;CK collections for threat detection in your organization.
-   **[Manage matrices](../task/view-mitre-collection.md)**  
Manage the matrices that have been imported from the MITRE TAXII collections. Matrices are a collection of tactics and techniques. You can view the matrices to review if your collections are available in the MITRE-ATT&amp;CK repository.
-   **[Manage techniques](../task/view-techniques.md)**  
Manage the techniques that have been imported from the MITRE TAXII collections. The techniques contain various ways attackers have developed to employ a given tactic. You can review and deactivate techniques that are not relevant to your organization. In STIX, techniques are known as attack patterns.
-   **[Manage mitigations](../task/manage-mitigations.md)**  
Manage the mitigations that have been imported from the MITRE TAXII collections. Mitigations enable you to prevent an adversary from successfully executing techniques or sub-techniques against your organization. In STIX, mitigations are known as course of actions.
-   **[Manage groups](../task/manage-groups-threat-intel.md)**  
Manage the groups that have been imported from the MITRE TAXII collections. Groups are sets of related intrusion activity that are tracked by a common name in the security community. Analysts track clusters of activities using various terms such as threat groups, activity groups, threat actors, intrusion sets, and campaigns. In STIX, groups are known as intrusion sets.
-   **[Manage malware](../task/manage-malware.md)**  
Manage the malware information that you imported from the MITRE TAXII collections. Malware is a type of TTP that represents malicious code. It refers to a program that is covertly inserted into a system. The intent of a malware is to compromise the confidentiality, integrity, or availability of the victim's data, applications, or operating system \(OS\).
-   **[Manage tools](../task/manage-tools.md)**  
Manage the tools information that you imported from the MITRE TAXII collections. Tools are legitimate software that are used by threat actors to perform attacks.
-   **[Manage MITRE relationships](../task/manage-mitre-relationships.md)**  
Manage the MITRE relationships information that you imported from the MITRE TAXII collections.
-   **[Manage CVE and technique mapping](../task/manage-cve-and-technique-mapping.md)**  
Manage the CVE and technique information that is mapped after you import the MITRE TAXII collections.
-   **[Extend the MITRE-ATT&amp;CK data](../task/view-and-extend-information.md)**  
Extend the MITRE-ATT&amp;CK repository data in the ServiceNow AI Platform by enriching it.
-   **[Define the data source and detection tool mapping](../task/manage-mitre-att-ck-data-sources.md)**  
Define the data source and detection tool mapping for MITRE-ATT&amp;CK tactics and techniques. The data source mapping provides you with insight into the relevance and availability of the data sources and the detection tools for monitoring the data sources in your environment.
-   **[Define the data source and data component mapping](../task/map-the-data-source-and-data-components.md)**  
Use the Data Component Mapping if you are using the latest TAXII collections, and you want to maintain a relationship between the data sources, data components, and the various techniques. Map the data sources with the additional context of data components that provides an extra sublayer of context to data sources that enable you to understand adversary behaviors in MITRE-ATT&amp;CK better.
-   **[Define the technique detection coverage](../task/define-technique-coverage.md)**  
Define the technique detection coverage that your organization must measure and detect specific adversary techniques.
-   **[Map your technique detection coverage to a technique](../task/map-technique-coverage.md)**  
Map your overall technique detection coverage with the technique that enables your organization to detect specific adversary techniques.
-   **[Define the mitigation coverage](../task/define-the-mitigation-coverage.md)**  
Define the mitigation coverage for each mitigation that is associated with a technique so that you gain visibility into how well your organization can prevent the attacks that happen due to a particular technique.
-   **[Map your mitigation coverage to a technique](../task/map-your-mitigation-coverage-to-a-technique.md)**  
Map your mitigation coverage with the technique that enables you to detect your organization's overall mitigation strategy.
-   **[Create and map detection rules](../task/create-detection-rules.md)**  
Create detection rules and map them against the tactics and techniques. With this mapping, you can see the coverage for the detection rules in your organization.
-   **[Auto-extract technique rules for importing MITRE-ATT&amp;CK information](auto-extract-technique-rules.md#)**  
Use the base system auto-extraction rules to import the MITRE-ATT&amp;CK information from any existing third-party integrations.
-   **[Review threat group and MITRE-ATT&amp;CK techniques mapping](../task/review-threat-group-and-techniques-mapping.md)**  
Review the threat group and techniques object to object relationship mapping information that is imported from the MITRE TAXII collections. This mapping enables you to view the technique group and the corresponding technique mapping.
-   **[Threat group to technique heatmap definition](../task/threat-group-to-technique-heatmap-definition.md)**  
Define the threat group to technique heatmap definition so that on the heatmap you can measure and detect the attack patterns that threat groups are using to attack your organization. The probability of an attack using a particular technique increases when you have a high number of attackers.
-   **[Review the MITRE-ATT&amp;CK system properties](../task/configure-mitre-att-ck-properties.md)**  
Review the MITRE-ATT&amp;CK system property values.

**Parent Topic:**[MITRE-ATT&amp;CK framework overview](about-mitre-attack.md)

**Related topics**  


[Using MITRE-ATT&amp;CK to detect and analyze threats](mitre-att-ck-features.md)

