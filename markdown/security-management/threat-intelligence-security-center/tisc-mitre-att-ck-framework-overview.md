---
title: MITRE-ATT&amp;CK repository
description: The MITRE-ATT&amp;CK repository stores MITRE data separately from Threat Intel Library data in the Intelligence Library.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/security-management/threat-intelligence-security-center/tisc-mitre-att-ck-framework-overview.html
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [MITRE ATT&amp;CK, threat intelligence, repository]
breadcrumb: [TISC Library Repository, Threat Intel Library, Use, Threat Intelligence Security Center, Security Operations]
---

# MITRE-ATT&amp;CK repository

The MITRE-ATT&amp;CK repository stores MITRE data separately from **Threat Intel Library** data in the **Intelligence Library**.

MITRE data is stored in a separate repository from **Threat Intel Library** data. MITRE data is not aggregated or deduplicated and remains independent.

The available data sources are:

-   **MITRE - Enterprise ATT&amp;CK**
-   **MITRE - Mobile ATT&amp;CK**
-   **MITRE - ICS ATT&amp;CK**

To create a MITRE source, configure a custom source. For more information, see [View Custom Feed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/view-oob-custom-feeds.md). In the form view, select the **Advanced** check box and set **Report Processor** to **MITRECollectionDataProcessor**.

## Revoked tactic and technique associations

A MITRE ATT&amp;CK release may revoke a technique or remove a technique-to-tactic mapping. When this occurs, the next MITRE ingestion retires the tactic and technique link, along with all entity and case associations built from it. Retirement is a soft delete. If MITRE restores a pair in a later release, the pair is reinstated automatically.

Retired associations are excluded from the MITRE ATT&amp;CK canvas, the technique cards, and the MITRE reports. The tactic and technique counts reflect only the mappings that MITRE currently publishes. The associations remain on the entity and case records until you delete or remap them. For more information on acting on a revoked pair, see [Review revoked MITRE tactic and technique associations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/tisc-review-revoked-mitre-associations.md).

The following lists are available under MITRE ATT&amp;CK in the Threat Intel Library:

-   **Tactics** — tactics that MITRE currently publishes
-   **Tactic-Techniques** — tactic and technique pairs that MITRE currently maps
-   **Revoked Tactic-Techniques** — the pairs that MITRE no longer maps and that still have entity or case associations for you to act on.

A MITRE ATT&amp;CK Associations section lists the entity and case associations that were derived from MITRE data, in the Entity Associations and Case Associations lists. Both lists exclude retired associations.

-   **[Manage Matrices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/tisc-manage-matrices.md)**  
Manage the matrices that are imported from the MITRE TAXII collections. Matrices are a collection of tactics and techniques. You can view the matrices to review if your collections are available in the MITRE-ATT&amp;CK repository.
-   **[Manage Techniques](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/tisc-manage-techniques.md)**  
Manage the techniques that are imported from the MITRE TAXII collections. The techniques contain various ways attackers have developed to employ a given tactic. You can review and deactivate techniques that are not relevant to your organization. In STIX, techniques are known as attack patterns.
-   **[Review revoked MITRE tactic and technique associations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/tisc-review-revoked-mitre-associations.md)**  
Review the tactic and technique pairs that MITRE no longer maps, then delete or remap the entity and case associations that were created from them.
-   **[Manage Mitigations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/tisc-manage-mitigations.md)**  
Manage the mitigations that are imported from the MITRE TAXII collections. Mitigations enable you to prevent an adversary from successfully executing techniques or sub-techniques against your organization. In STIX, mitigations are known as course of actions.
-   **[Manage Groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/tisc-manage-groups.md)**  
Manage the groups that are imported from the MITRE TAXII collections. Groups are sets of related intrusion activity that are tracked by a common name in the security community. Analysts track clusters of activities using various terms such as threat groups, activity groups, threat actors, intrusion sets, and campaigns. In STIX, groups are known as intrusion sets.
-   **[Manage Malware](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/tisc-manage-malware.md)**  
Manage the malware information that you imported from the MITRE TAXII collections. It is a type of TTP that represents malicious code.
-   **[Manage Tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/tisc-mitre-manage-tools.md)**  
Manage the tools information that you imported from the MITRE TAXII collections. Tools are legitimate software that are used by threat actors to perform attacks.
-   **[Manage MITRE Relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/tisc-mitre-manage-relationships.md)**  
Manage the MITRE relationships information that you imported from the MITRE TAXII collections.

**Parent Topic:**[TISC Library Repository](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/tisc-ioc.md)

**Related topics**  


[Observables]()

[Indicators]()

[Threat Entities]()

[Other Objects]()

[Vulnerability Artifacts]()

[View RSS Feeds]()

[Working with Reports in TISC]()

[Relationships Objects]()

[Potential Relationships]()

[Vulnerability relationship mapping]()

