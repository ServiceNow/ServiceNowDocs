---
title: Threat group to technique heatmap definition
description: Define the threat group to technique heatmap definition so that on the heatmap you can measure and detect the attack patterns that threat groups are using to attack your organization. The probability of an attack using a particular technique increases when you have a high number of attackers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-group-to-technique-heatmap-definition.html
release: australia
topic_type: task
last_updated: "2026-03-12"
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

    The following illustration shows the threat group to technique heat map definitions list.\[Omitted image "mitre-threat-group-definition.png"\] Alt text: The following illustration shows the threat group to technique heat map definitions list.

3.  To add an entry, click **New**, complete the entries, and click **Submit**.


**Parent Topic:**[MITRE-ATT&amp;CK administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/mitre-att-ck-administration.md)

**Related topics**  


[Get started with MITRE-ATT&amp;CK framework]()

[Understand the MITRE to STIX data model]()

[Domain separation and MITRE-ATT&amp;CK]()

[Set up the MITRE-ATT&amp;CK framework]()

[Manage matrices]()

[Manage techniques]()

[Manage mitigations]()

[Manage groups]()

[Manage malware]()

[Manage tools]()

[Manage MITRE relationships]()

[Manage CVE and technique mapping]()

[Extend the MITRE-ATT&amp;CK data]()

[Define the data source and detection tool mapping]()

[Define the data source and data component mapping]()

[Define the technique detection coverage]()

[Map your technique detection coverage to a technique]()

[Define the mitigation coverage]()

[Map your mitigation coverage to a technique]()

[Create and map detection rules]()

[Auto-extract technique rules for importing MITRE-ATT&amp;CK information]()

[Review threat group and MITRE-ATT&amp;CK techniques mapping]()

[Review the MITRE-ATT&amp;CK system properties]()

