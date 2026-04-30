---
title: Threat group to technique heatmap definition
description: Define the threat group to technique heatmap definition so that on the heatmap you can measure and detect the attack patterns that threat groups are using to attack your organization. The probability of an attack using a particular technique increases when you have a high number of attackers.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [MITRE-ATT&amp;CK administration, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Threat group to technique heatmap definition

Define the threat group to technique heatmap definition so that on the heatmap you can measure and detect the attack patterns that threat groups are using to attack your organization. The probability of an attack using a particular technique increases when you have a high number of attackers.

## Before you begin

Role required:

-   sn\_ti.admin, sn\_si.admin: write access
-   sn\_ti.read: read access

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **MITRE ATT&amp;CK Administration** &gt; **Threat Group-Technique Heat Map Definition**.

2.  Review the threat group to technique heatmap definition and customize the entries for your environment.

<table id="table_tm2_qx2_vrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number of Threat Groups \(min range\)

</td><td>

The minimum number of threat groups using a particular technique.

</td></tr><tr><td>

Number of Threat Groups \(max range\)

</td><td>

The maximum number of threat groups using a particular technique. The probability of an attack using a particular technique increases when you have a high number of attackers.

</td></tr><tr><td>

Heat Map Color

</td><td>

Color that is assigned to the threat group category. The color that you define is used to highlight the threat group category in the heat map.You can customize the colors using HEX codes and RGB\(A\) values.

</td></tr><tr><td>

Text Color

</td><td>

Color that is assigned to the threat group text. The color that you define is used to highlight the threat groups in the heat map.You can customize the colors using HEX codes and RGB\(A\) values.

</td></tr><tr><td>

Description

</td><td>

Description about the threat group range and definition.

</td></tr></tbody>
</table>    **Note:** Ensure that you do not overlap the threat group count ranges if you customize the threat group range \(min or max\).

    The following illustration shows the threat group to technique heat map definitions list.![The following illustration shows the threat group to technique heat map definitions list.](../image/mitre-threat-group-definition.png)

3.  To add an entry, click **New**, complete the entries, and click **Submit**.


**Parent Topic:**[MITRE-ATT&amp;CK administration](../concept/mitre-att-ck-administration.md)

**Related topics**  


[Get started with MITRE-ATT&amp;CK framework](../reference/get-started-with-mitre.md)

[Understand the MITRE to STIX data model](../reference/understand-the-mitre-to-stix-data-model-mapping.md)

[Domain separation and MITRE-ATT&amp;CK](../reference/domain-separation-and-mitre-att-ck.md)

[Set up the MITRE-ATT&amp;CK framework](setup-mitre-profile.md)

[Manage matrices](view-mitre-collection.md)

[Manage techniques](view-techniques.md)

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

[Review the MITRE-ATT&amp;CK system properties](configure-mitre-att-ck-properties.md)

