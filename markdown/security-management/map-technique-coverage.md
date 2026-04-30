---
title: Map your technique detection coverage to a technique
description: Map your overall technique detection coverage with the technique that enables your organization to detect specific adversary techniques.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [MITRE-ATT&amp;CK administration, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Map your technique detection coverage to a technique

Map your overall technique detection coverage with the technique that enables your organization to detect specific adversary techniques.

## Before you begin

-   Role required: sn\_ti.admin, sn\_si.admin: write access
-   Role required: sn\_ti.read: read access

## About this task

You can use the technique detection coverage to get an overview into your organization's overall technique detection coverage. For example, if an adversary is attacking your organization, you see the kind of coverage that you have to detect the attacker's techniques.

The technique and ID are automatically populated for all the [collections](setup-mitre-profile.md) and [techniques](view-techniques.md) that you have activated. The [coverage type and scoring definition](define-technique-coverage.md) that you have defined are available for as an option that you can select in the overall technique detection coverage.

You can map the overall technique detection coverage with the technique to complete the mapping. You can associate a technique with only one overall technique detection coverage.

The technique detection coverage mapping that you define is used in the [coverage visualization in the heatmap](../concept/mitre-att-ck-heatmap-and-navigator.md#).

**Note:** You can arrive at the overall technique detection coverage using your organization-specific calculations. You may use any Breach &amp; Attack Simulation \(BAS\) products, the Cyber Analytics Repository \(CAR\), or any other methods as necessary to define the scoring definition, and use it in this procedure for the overall technique detection coverage mapping.

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **MITRE ATT&amp;CK Administration** &gt; **Detection Coverage Mapping**.

    In this illustration, you see that the Cloud Accounts \(T1078.004\) sub-technique has excellent coverage in the organization and that the Overall Technique Detection Coverage is mapped to **Excellent**.

    ![Detection coverage mapping.](../image/mitre-coverage-mapping.gif)

2.  Review each technique and map your overall technique detection coverage based on your [detection coverage definition](define-technique-coverage.md) and your organization's coverage availability.


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

[Define the mitigation coverage](define-the-mitigation-coverage.md)

[Map your mitigation coverage to a technique](map-your-mitigation-coverage-to-a-technique.md)

[Create and map detection rules](create-detection-rules.md)

[Auto-extract technique rules for importing MITRE-ATT&amp;CK information](../concept/auto-extract-technique-rules.md#)

[Review threat group and MITRE-ATT&amp;CK techniques mapping](review-threat-group-and-techniques-mapping.md)

[Threat group to technique heatmap definition](threat-group-to-technique-heatmap-definition.md)

[Review the MITRE-ATT&amp;CK system properties](configure-mitre-att-ck-properties.md)

