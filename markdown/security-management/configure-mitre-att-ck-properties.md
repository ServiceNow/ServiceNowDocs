---
title: Review the MITRE-ATT&amp;CK system properties
description: Review the MITRE-ATT&amp;CK system property values.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/configure-mitre-att-ck-properties.html
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

Rollup of MITRE-ATT&amp;CK information from observables to the security incident. For more information, see [Associate MITRE ATT&amp;CK information with observables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/associate-mitre-observables.md).

 Default value: Yes

</td></tr><tr><td>

Roll up MITRE ATT&amp;CK information automatically from Threat Lookup results to security incident\[sn\_ti.rollup\_mitre\_att&amp;ck\_technique\_threat\_lookup\_si\]

</td><td>

Rollup of MITRE-ATT&amp;CK information from threat lookup results to the security incident. For more information, see [Threat lookup auto-extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/auto-extract-technique-rules.md).Default value: Yes

</td></tr><tr><td>

Roll up MITRE ATT&amp;CK information automatically from alert rules to security incidents\[sn\_ti.rollup\_mitre\_att&amp;ck\_technique\_alert\_rule\_si\]

</td><td>

Rollup of MITRE-ATT&amp;CK TTP information automatically from alert rules to security incidents. For more information, see [map detection rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/create-detection-rules.md).Default value: No

</td></tr><tr><td>

Roll up MITRE ATT&amp;CK information automatically from child security incidents to parent security incident\[sn\_ti.rollup\_mitre\_att&amp;ck\_technique\_child\_si\_si\]

</td><td>

Roll up MITRE-ATT&amp;CK information automatically from child security incidents to parent security incident. Default value: Yes

</td></tr><tr><td>

Enabling this property allows mapping of Security Incident Fields like category and sub category with Detection Rules in "Detection Rules - MITRE ATT&amp;CK mapping" table\[sn\_ti.enable\_category\_mapping\_with\_alert\_rule\]

</td><td>

Category and sub-category in the [Detection Rules - MITRE ATT&amp;CK mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/create-detection-rules.md) page.

 Default value: No

</td></tr><tr><td>

Time\(in hours\) to calculate "CVE - VUL Count"\[sn\_ti.time\_to\_calculate\_cve\_vits\_count\]

</td><td>

The scheduled time in hours to calculate the CVE and VUL information.Default value: 24

</td></tr></tbody>
</table>3.  Click **Save**.


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

[Threat group to technique heatmap definition]()

