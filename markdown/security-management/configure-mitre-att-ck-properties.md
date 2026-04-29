---
title: Review the MITRE-ATT&amp;CK system properties
description: Review the MITRE-ATT&amp;CK system property values.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [MITRE-ATT&amp;CK administration, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Review the MITRE-ATT&amp;CK system properties

Review the MITRE-ATT&amp;CK system property values.

## Before you begin

Role required: sn\_ti.admin, sn\_si.admin

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **MITRE ATT&amp;CK Administration** &gt; **Properties**.

2.  On the form, fill in the fields.

<table id="table_bpn_2wt_wnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Roll up MITRE ATT&amp;CK information automatically from Observables to security incident\[sn\_ti.rollup\_mitre\_att&amp;ck\_technique\_observable\_si\]

</td><td>

Rollup of MITRE-ATT&amp;CK information from observables to the security incident. For more information, see [Associate MITRE ATT&amp;CK information with observables](associate-mitre-observables.md).

 Default value: Yes

</td></tr><tr><td>

Roll up MITRE ATT&amp;CK information automatically from Threat Lookup results to security incident\[sn\_ti.rollup\_mitre\_att&amp;ck\_technique\_threat\_lookup\_si\]

</td><td>

Rollup of MITRE-ATT&amp;CK information from threat lookup results to the security incident. For more information, see [Threat lookup auto-extraction](../concept/auto-extract-technique-rules.md#).Default value: Yes

</td></tr><tr><td>

Roll up MITRE ATT&amp;CK information automatically from alert rules to security incidents\[sn\_ti.rollup\_mitre\_att&amp;ck\_technique\_alert\_rule\_si\]

</td><td>

Rollup of MITRE-ATT&amp;CK TTP information automatically from alert rules to security incidents. For more information, see [map detection rules](create-detection-rules.md).Default value: No

</td></tr><tr><td>

Roll up MITRE ATT&amp;CK information automatically from child security incidents to parent security incident\[sn\_ti.rollup\_mitre\_att&amp;ck\_technique\_child\_si\_si\]

</td><td>

Roll up MITRE-ATT&amp;CK information automatically from child security incidents to parent security incident. Default value: Yes

</td></tr><tr><td>

Enabling this property allows mapping of Security Incident Fields like category and sub category with Detection Rules in "Detection Rules - MITRE ATT&amp;CK mapping" table\[sn\_ti.enable\_category\_mapping\_with\_alert\_rule\]

</td><td>

Category and sub-category in the [Detection Rules - MITRE ATT&amp;CK mapping](create-detection-rules.md) page.

 Default value: No

</td></tr><tr><td>

Time\(in hours\) to calculate "CVE - VUL Count"\[sn\_ti.time\_to\_calculate\_cve\_vits\_count\]

</td><td>

The scheduled time in hours to calculate the CVE and VUL information.Default value: 24

</td></tr></tbody>
</table>3.  Click **Save**.


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

[Threat group to technique heatmap definition](threat-group-to-technique-heatmap-definition.md)

