---
title: Manage techniques
description: Manage the techniques that have been imported from the MITRE TAXII collections. The techniques contain various ways attackers have developed to employ a given tactic. You can review and deactivate techniques that are not relevant to your organization. In STIX, techniques are known as attack patterns.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [MITRE-ATT&amp;CK administration, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Manage techniques

Manage the techniques that have been imported from the MITRE TAXII collections. The techniques contain various ways attackers have developed to employ a given tactic. You can review and deactivate techniques that are not relevant to your organization. In STIX, techniques are known as attack patterns.

## Before you begin

Role required:

-   sn\_ti.admin: delete access
-   sn\_si.admin: create, write, delete access
-   sn\_ti.read: read access
-   sn\_ti.write: create, write access

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **MITRE ATT&amp;CK Repository** &gt; **Techniques**.

    ![View the list of techniques and sub-techniques.](../image/techniques-list.png)

    The list of techniques and subtechniques are now listed.

2.  To review and deactivate techniques that are not relevant to your organization, go to the list view for the selected technique, and under the Active column, update the setting to **false**, and save the setting.

    Deactivate the techniques that aren't used by the other objects in the MITRE-ATT&amp;CK repository.

3.  To prioritize a technique, assign a priority in the **Relevant Priority \(Custom\)** field.

    The base system relevant priority is set to none. The **Relevant Priority \(Custom\)** field is not imported from the MITRE-ATT&amp;CK TAXII collections but a custom field introduced in the ServiceNow AI Platform. You can use the relevant priority information to filter and prioritize techniques in the dashboards, during the data source mapping, or when analyzing the heat map.

4.  Click a technique to view all the associated information with this technique.

    In the following illustration, you can view the details for each Account Access Removal technique, its ID, source, and other related information.

    ![View the attack pattern technique and it's related information.](../image/mitre-technique-attack-pattern.jpg)

    **Note:** The Data Source: Data Component element introduced by MITRE replaces the previous Data Source field. Data component provides an extra sublayer of context to the data sources. If your MITRE-ATT&amp;CK repository contains the old TAXII collections, then you can view the Data Source field. Otherwise, you can view the data sources with the additional context of data components in the Data Source: Data Component field. You can view the new data component field only when the source is Enterprise ATT&amp;CK. For more information, see [data component mapping](map-the-data-source-and-data-components.md).

5.  To view how these objects are related, click **Show Relationships**.


## What to do next

You can [extend the information](view-and-extend-information.md) in some of these related list objects. For example, you can add new information for Group, Mitigation, and External References.

**Parent Topic:**[MITRE-ATT&amp;CK administration](../concept/mitre-att-ck-administration.md)

**Related topics**  


[Get started with MITRE-ATT&amp;CK framework](../reference/get-started-with-mitre.md)

[Understand the MITRE to STIX data model](../reference/understand-the-mitre-to-stix-data-model-mapping.md)

[Domain separation and MITRE-ATT&amp;CK](../reference/domain-separation-and-mitre-att-ck.md)

[Set up the MITRE-ATT&amp;CK framework](setup-mitre-profile.md)

[Manage matrices](view-mitre-collection.md)

[Manage mitigations](manage-mitigations.md)

[Manage groups](manage-groups-threat-intel.md)

[Manage malware](manage-malware.md)

[Manage tools](manage-tools.md)

[Manage MITRE relationships](manage-mitre-relationships.md)

[Manage CVE and technique mapping](manage-cve-and-technique-mapping.md)

[Extend the MITRE-ATT&amp;CK data](view-and-extend-information.md)

[Define the data source and detection tool mapping](manage-mitre-att-ck-data-sources.md)

[Define the data source and data component mapping](map-the-data-source-and-data-components.md)

[Define the technique detection coverage](define-technique-coverage.md)

[Map your technique detection coverage to a technique](map-technique-coverage.md)

[Define the mitigation coverage](define-the-mitigation-coverage.md)

[Map your mitigation coverage to a technique](map-your-mitigation-coverage-to-a-technique.md)

[Create and map detection rules](create-detection-rules.md)

[Auto-extract technique rules for importing MITRE-ATT&amp;CK information](../concept/auto-extract-technique-rules.md#)

[Review threat group and MITRE-ATT&amp;CK techniques mapping](review-threat-group-and-techniques-mapping.md)

[Threat group to technique heatmap definition](threat-group-to-technique-heatmap-definition.md)

[Review the MITRE-ATT&amp;CK system properties](configure-mitre-att-ck-properties.md)

