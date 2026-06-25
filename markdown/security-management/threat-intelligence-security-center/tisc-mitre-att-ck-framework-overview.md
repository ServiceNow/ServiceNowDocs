---
title: MITRE-ATT&amp;CK Repository
description: The MITRE-ATT&amp;CK repository is available under the Intelligence Library where the data from the MITRE sources are ingested.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-mitre-att-ck-framework-overview.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# MITRE-ATT&amp;CK Repository

The MITRE-ATT&amp;CK repository is available under the Intelligence Library where the data from the MITRE sources are ingested.

The MITRE data that is coming to the repository is stored in a separate MITRE repository from Threat Intel Library data, where MITRE data isn’t rolled up for aggregation or de-duplication flow and is independent.

The available data sources within the application are:

1.  MITRE - Enterprise ATT&amp;CK
2.  MITRE - Mobile ATT&amp;CK
3.  MITRE - ICS ATT&amp;CK

The data for these sources are stored in a separate MITRE repository under TI library in the base system. In case, if you want to create a new MITRE source then configure a custom source. For more information, see [View Custom Feed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/view-oob-custom-feeds.md) and in the form view click **Advanced** check box and select the **Report Processor** as: **MITRECollectionDataProcessor**.

-   **[Manage Matrices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-manage-matrices.md)**  
Manage the matrices that are imported from the MITRE TAXII collections. Matrices are a collection of tactics and techniques. You can view the matrices to review if your collections are available in the MITRE-ATT&amp;CK repository.
-   **[Manage Techniques](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-manage-techniques.md)**  
Manage the techniques that are imported from the MITRE TAXII collections. The techniques contain various ways attackers have developed to employ a given tactic. You can review and deactivate techniques that are not relevant to your organization. In STIX, techniques are known as attack patterns.
-   **[Manage Mitigations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-manage-mitigations.md)**  
Manage the mitigations that are imported from the MITRE TAXII collections. Mitigations enable you to prevent an adversary from successfully executing techniques or sub-techniques against your organization. In STIX, mitigations are known as course of actions.
-   **[Manage Groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-manage-groups.md)**  
Manage the groups that are imported from the MITRE TAXII collections. Groups are sets of related intrusion activity that are tracked by a common name in the security community. Analysts track clusters of activities using various terms such as threat groups, activity groups, threat actors, intrusion sets, and campaigns. In STIX, groups are known as intrusion sets.
-   **[Manage Malware](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-manage-malware.md)**  
Manage the malware information that you imported from the MITRE TAXII collections. It is a type of TTP that represents malicious code.
-   **[Manage Tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-mitre-manage-tools.md)**  
Manage the tools information that you imported from the MITRE TAXII collections. Tools are legitimate software that are used by threat actors to perform attacks.
-   **[Manage MITRE Relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-mitre-manage-relationships.md)**  
Manage the MITRE relationships information that you imported from the MITRE TAXII collections.

**Parent Topic:**[TISC Library Repository](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-ioc.md)

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

